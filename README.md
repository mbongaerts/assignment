# Python Opdracht: Warmtevraagmodellering voor een Huishouden

## Inleiding

Bedankt voor je interesse in de functie van Python Programmeur bij CE Delft! Deze opdracht is bedoeld om je Python- en Git-vaardigheden te testen. Je gaat een eenvoudig thermodynamisch model bouwen dat de warmtevraag van een huishouden berekent op basis van een jaarlijkse temperatuursreeks en de isolatiegraad van de woning. Vervolgens modelleer je hoe een all-electric warmtepomp deze vraag invult.

## Opdrachtomschrijving

### Doel

Schrijf een Pythonmodel dat:

1. De warmtevraag van een huishouden berekent op uurbasis (in kWh/uur).
2. Het totale elektriciteitsverbruik van een all-electric warmtepomp berekent om aan deze warmtevraag te voldoen.
3. Een grafiek genereert met de warmtevraag (kWh/uur) en het totale verbruik van de warmtepomp (in kWh).

### Inputs

- Een CSV-bestand met een jaarlijkse temperatuursreeks (temperatuur per uur, in °C).
- De isolatiegraad van de woning, uitgedrukt als een warmteoverdrachtcoëfficiënt (in W/K).

### Model

Gebruik het volgende eenvoudige thermodynamische model:

- **Warmtevraag (Q, in kWh/uur)**:  
`Q = U * (T_setpoint - T_outside) / 1000`
  - `U`: Warmteoverdrachtcoëfficiënt (W/K). Schat een realistisch getal in op basis van literatuur.
  - `T_setpoint`: Streeftemperatuur in de woning (bijv. 20°C). **Bonus: veriëer de set-point temperatuur voor dag en nacht.**
  - `T_outside`: Buitentemperatuur per uur (°C)
- **Warmtepompverbruik (E, in kWh)**:  
`E = Q / COP`
  - `COP`: Coëfficiënt of Performance van de warmtepomp. Maak deze afhankelijk van de buitentemperatuur. Zoek zelf naar literatuur voor een correcte COP-formule.

### Outputs

- Een grafiek met de warmtevraag (kWh/uur) over het jaar.
- Het totale verbruik van de warmtepomp (in kWh).

### Vereisten

- Gebruik Python 3.11 of hoger.
- Gebruik `pandas` voor data-verwerking en `plotly` voor visualisatie.
- Schrijf duidelijke, goed gedocumenteerde code met type hints.
- Voeg een `requirements.txt` toe met de benodigde packages.

### Stappenplan

1. **Data inlezen**: Lees de jaarlijkse temperatuursreeks uit een CSV-bestand; download deze van het KNMI: https://daggegevens.knmi.nl/klimatologie/uurgegevens. Gebruik station De Bilt, en een klimaatjaar naar keuze.
2. **Warmtevraag berekenen**: Bereken de warmtevraag per uur met bovenstaand model.
3. **Warmtepompverbruik berekenen**: Bereken het verbruik per uur en som dit op voor het totale jaarverbruik.
4. **Visualisatie**: Maak een grafiek van de warmtevraag en het elektrische verbruik per uur (over het hele jaar).
5. **Output**: Sla de resultaten op in een excelbestand en sla de grafiek op als png of html.

---

## Git Instructies

### Repository

1. **Fork** deze repository naar je eigen GitHub-account.
2. **Clone** de geforkte repository naar je lokale machine.
3. Maak een nieuwe branch aan met je naam (bijv. `voornaam-achternaam`).
4. Voeg je oplossing toe aan deze branch.
5. **Commit** en **push** je wijzigingen naar je geforkte repository.
6. Maak een **Pull Request** naar de originele repository.

### Commit Berichten

- Gebruik duidelijke commit berichten (bijv. "Voeg warmtevraagberekening toe").
- Commit regelmatig, zodat je voortgang zichtbaar is.

### Pull Request

- Zorg dat je code werkt en alle vereisten vervult.
- Voeg een korte beschrijving toe aan je Pull Request.

---

## Beoordelingscriteria

- Correctheid van de berekeningen.
- Kwaliteit en leesbaarheid van de code.
- Gebruik van Git (commits, branches, Pull Request).

---

## Deadline

Lever je oplossing uiterlijk [deadline invullen] in via een Pull Request.

Succes!