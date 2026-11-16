# Loop de route

Werkvorm-app voor het project M6 BO museum-app (Mediacollege Amsterdam, Software Developer).
Groepjes van drie testen elkaars user journey en briefing en bespreken de haalbaarheid van hun project.

## Gebruik

De app is een enkele pagina: `index.html`. Er is geen installatie of build nodig.

1. Studenten doorlopen zeven stappen: Groepje, Rode draad, Zelfcontrole, Loop de route, Haalbaarheid, Top 3 en Inleveren.
2. Bij Inleveren downloaden ze een JSON-bestand en leveren dat in.
3. De docent laadt de JSON-bestanden op het tabblad "Importeren en review".

Gegevens blijven in de browser van het apparaat (localStorage). Er wordt niets verstuurd.

## GitHub Pages aanzetten

1. Ga in de repository naar Settings > Pages.
2. Kies bij "Source" voor "Deploy from a branch".
3. Kies de branch `main` en de map `/ (root)` en klik op Save.
4. Na ongeveer een minuut staat de app op `https://<gebruikersnaam>.github.io/<repository>/`.

## Aanpassen

Alles staat bovenaan het script in `index.html`:

- `SCENARIOS`: de scenariokaarten voor Peter en Daan
- `STAPPEN`: de stappen en de tijd per stap in minuten
- `VRAGEN`: de vragen per stap
- `UITLEG`: de uitleg en het schema per stap
- `ROLLEN`: de drie rollen per stap (de app verdeelt ze over de drie leden)
