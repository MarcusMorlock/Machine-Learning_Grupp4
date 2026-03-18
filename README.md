# Grupp 4 – Marketplace Safety
 
Detta projekt är en gruppuppgift i Machine Learning där målet är att bygga ett beslutsstöd för att prioritera misstänkta händelser på en marknadsplats.
 
## Projektets mål
Vi ska bygga en klassificeringsmodell som bedömer om en händelse är misstänkt eller inte. Syftet är inte att få allt rätt, utan att skapa en lösning som fungerar rimligt bra på ny data, går att köra regelbundet och går att förklara för icke-tekniska personer.

## Data
Projektet använder två filer i projektets rotmapp:
- `historical_data.csv` för träning, test och modellutvärdering
- `new_data.csv` för prediktion på ny, osedd data

## Verktyg och paket
- Python 3.13.7
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
 
Random state: 42
 
## Hur man kör projektet
1. Klona repot från GitHub
2. Skapa och aktivera en virtuell miljö
3. Installera paketen med `python -m pip install -r requirements.txt`
4. Kontrollera att `historical_data.csv` och `new_data.csv` finns i projektets rotmapp
5. Öppna `report.ipynb` i VS Code eller Jupyter
6. Kör notebooken med `Restart & Run All`
 
## Kravkort
Vi pitchar till Lina, Customer Support Lead.
 
Det viktigaste i vår lösning är att hålla nere onödiga flaggningar och att det som flaggas känns rimligt och konsekvent. Vi behöver också tänka på användarupplevelsen och undvika att skada förtroendet för plattformen.
 
## Vår strategi
Vi bygger en klassificeringsmodell för att bedöma om en händelse är misstänkt eller inte. Eftersom vårt kravkort fokuserar på att minska onödiga flaggningar prioriterar vi en försiktig lösning. Därför fokuserar vi på precision och väljer en threshold eller prioriteringsregel som inte flaggar för aggressivt.
 
Vi använder en pipeline för att hantera preprocessing på ett sätt som minskar risken för data leakage. Vi jämför flera modeller, väljer en slutmodell, gör enkel hyperparameter-tuning och använder sedan modellen för att prioritera nya observationer.
 
## Ansvarsfördelning
- Jonas: Data och EDA
- Marcus: Pipeline och preprocessing
- Henry: Modelljämförelse
- Henrik: Optimering och presentation
- Ali: Threshold, prioritering och resultat på new_data.csv
 
## Resultat på ny data
Projektet innehåller även en tillämpning av den färdiga och låsta pipelinen på `new_data.csv`. Eftersom `new_data.csv` saknar target används filen inte för utvärdering med precision eller recall, utan för att skapa en prioriteringslista för manuell granskning. Med vårt valda tröskelvärde på 0.62 flaggade modellen 7 händelser av totalt 2000 nya observationer.