# Loop de route

Werkvorm-app voor MBO-4 studenten Software Developer (Mediacollege Amsterdam), project M6 BO museum-app.
Wordt gehost op GitHub Pages vanaf de root van de branch `main`.

## Opbouw

- Een enkel bestand: `index.html` met HTML, CSS en JavaScript. Geen build, geen afhankelijkheden, geen backend.
- Schermen worden opgebouwd met de hulpfunctie `el()`. Tekst van gebruikers gaat altijd via `textContent`, nooit via `innerHTML`.
- Gegevens staan in localStorage onder de sleutel `loop-de-route-v2`, altijd binnen try/catch.
- Export en import gebruiken JSON met `app: "loop-de-route"` en `versie: 3`. Verandert de vorm van de gegevens, verhoog dan `versie` en pas `geldig()` en `vulAan()` aan. Bestanden van versie 2 (met `leden` als tekst) zet `vulAan()` om naar versie 3 (met `namen` als lijst van vier; de vierde plek is leeg bij een groepje van drie).
- Inhoud staat in de lijsten `PERSONAS`, `SCENARIOS`, `STAPPEN`, `VRAGEN`, `UITLEG`, `ROLLEN` en `ICONEN` bovenaan het script.
- Een groepje heeft drie of vier leden. `ROLLEN` geeft per stap vier rollen; de vierde is voor een groepje van vier. De app schuift de rollen elke stap een plek door.
- Tekeningen zijn SVG en worden gemaakt met `sv()`, `icoon()`, `avatar()` en `tafel()`. Iconen zijn versiering (`aria-hidden`). Een tekening met betekenis krijgt `role="img"` en een `aria-label`.
- Bij Inleveren staan twee exports: het JSON-bestand voor de docent en de blogtekst voor Simulise (`blog()`). In de blogtekst blijft het kopje "Mijn samenvatting" leeg. Dat vult elke student zelf in, in Simulise.
- `teken()` bouwt het scherm opnieuw op. Geef elke knop die `teken()` aanroept een `data-f`, dan blijft de focus op die knop. Zet `ui.focus` als de focus ergens anders heen moet. Berichten voor schermlezers gaan via `meld()`.

## Regels voor tekst en stijl

- Nederlands op taalniveau 2F: korte zinnen, zakelijk en duidelijk. Geen emoticons.
- De app voelt als een app: weinig tekst per scherm, uitleg in een schema met iconen, geen lange alinea's.
- Huisstijl: Arial, zwart, wit en magenta (#FF00CA).
- Toegankelijk: elk invoerveld heeft een label, alles werkt met het toetsenbord, en animaties staan uit bij `prefers-reduced-motion`.

## Testen

Open `index.html` in een browser. Doorloop alle zeven stappen met alleen het toetsenbord, kopieer de blogtekst, download het JSON-bestand en laad het weer in op het tabblad "Importeren en review".
