# KPIF Inflation Forecasting

Tidsserieanalys och prognosticering av svensk KPIF-inflation med data från Konjunkturinstitutet.

## Innehåll
Projektet består av två parallella analysspår:
- Spår A: Direkt modellering av rullande 12-månadersinflation (YoY)
- Spår B: Modellering av månadsförändring (MoM) med rekonstruktion till årstakt

Båda spåren utvärderas med expanding window pseudo out-of-sample prognoser på horisonterna h=1, 3, 6 och 12 månader, benchmarkade mot naive- och mean-prognoser.

## Data
`KPIF&OTHER.csv` från Konjunkturinstitutet. Placeras i `/data/`.

## Köra projektet
```
bash
pip install -r requirements.txt
jupyter notebook
```
Öppna och kör `notebook.ipynb` uppifrån och ned.

## Huvudresultat
*   AR(1) med covid-dummy presterar konsekvent bäst bland skattade modeller. 
*   MoM-rekonstruktionen ger bättre kortsiktiga prognoser (h=1-3), 
    medan direkt AR(1) på 12m-serien är mer stabil på längre horisonter (h=12) 
    under normala inflationsförhållanden.