# Potential economic effect of indexation formula on Ukrainian public procurement market

Public procurement of natural gas in Ukraine lacks stability and transparency: while contract data is publicly available via [ProZorro](https://prozorro.gov.ua/), contracting parties usually agree upon new prices in additional agreements, which are not available in machine-readable format. Objective price volatility does not explain all of the price fluctuations on the procurement market, so Ministry of Economy offered a formula to regulate the changes in price synchronously to the prices on European hubs (primarily [NCG](https://www.powernext.com/futures-market-data)).

Our task was to assess potential economic effect of introducing indexation formula. Machine-readable data from ProZorro API was complemented by students and volunteers, who manually checked the prices and supply schedules according to the additional agreements. After the data had been aggregated, we calculated the effect and created some vizualizations.

## Scripts description
* **00_addcontr_get_data** - getting natural gas data and docs from ProZorro
* **01_addcontr_explore** - basic exploration of the raw data
* **02_addcontr_distribute** - generate data extracts for students and volunteers
* **03_addcontr_aggregate_data** - check and aggregate datasets, complemented by students and volunteers
* **04_addcontr_count_savings** - refine data and calculate potential economic effect of price indexation formula
* **05_addcontr_describe_output** - create vizualizations

## Folders description
* **00_contracts_pdf** - sample of pdf files with additional contracts, structured by date and ProZorro's contract id
* **02_data** - raw data used for calculations, including:
  * *PNCGMc1_2019-01-14.csv* - NCG Month+1 daily natural gas prices
  * *exchange_rates_eur_2018_12_30.csv* - hryvnia to euro daily exchange rates
  * *prices_ueb_2019_01.csv* - Ukrainian Energy Exchange monthly natural gas prices
* **03_for_students** - distributed extracts from the main dataset, which were later completed by the students and volunteers, as well as a file to track the distributed contract ids
* **04_output** - aggregated data after the complements, as well as dataset with final calculations
* **05_viz** - vizualizations of calculated economic effects
