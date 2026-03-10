# Grupp 4 – Marketplace Safety
 
Detta projekt är en gruppuppgift i Machine Learning där målet är att bygga ett beslutsstöd för att prioritera misstänkta händelser på en marknadsplats.
 
## Projektets mål
Vi ska bygga en klassificeringsmodell som bedömer om en händelse är misstänkt eller inte. Syftet är inte att få allt rätt, utan att skapa en lösning som fungerar rimligt bra på ny data, går att köra regelbundet och går att förklara för icke-tekniska personer.
 
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
3. Installera nödvändiga paket
4. Öppna notebooken `report.ipynb`
5. Kör notebooken med `Restart & Run All`
 
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
- Henrik: Optimering
- Ali: Threshold och prioritering
 
## Kommentar
Vid redovisningen visar vi också vårt resultat på new_data.csv, hur många observationer vi flaggar och en kort reflektion kring risker, begränsningar och nästa steg.