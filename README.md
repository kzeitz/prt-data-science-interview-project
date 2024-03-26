# PRT Data Science Project

Real time price forecast for CAISO NP15. 

## Project Description

### Expectations
Generate a multi-step forecast model for CAISO NP15 mWh 
prices, capable of predicting 7 days (or 168 hours) worth of forecasts 
for each prediction.

### Data
The most common drivers of energy prices and energy price changes are weather 
and energy demand. We have attached the historic records for the respective 
region's energy demand `Load.act` as well as an aggregate temperature file 
for the region's temperature `Temp.act`. As well as the historic prices of 
the region starting 2013 `Price.act`.

#### Data Format
All attached data files are white space separated text files without headers 
containing 27 columns. First three columns are year, month and day and the 
consecutive columns are hourly prices for the 1st to the 24th hour of the 
respective date.

### Additional considerations
1. There are other factors and drivers contributing to energy prices. Some 
can be modeled.
2. The data shared is from real-life sources. It can be noisy, but 
it has not been manipulated for the purpose of the excercise.
3. We have attached a map of the forecast region `MapForecastRegion.png`. 
**Please note**, the here provided real time prices are for both, the 
NP15 and ZP26 region combined. In other there's one set of labels for both 
regions, which is commonly refereed to as NP15.

### Evaluation
You're not expected to hand in any model as a result of your work. As we 
have no intentions to test model accuracy beyond anything you want to 
show us in your project presentation. Consequently, we have not reserved 
any test data.

Your project will be evaluated based on the presentation of your work. You 
should be able to walks us through your approach, as well as reason about 
potential problems encountered and discuss alternative solutions or 
additional areas of research.

**Please note**, we do believe developing a model will aid in reasoning about 
the project.

## Helper Code
Attached you should find a python file `utils.py` containing a code snippet to read the 
attached data files into a pandas DataFrame `load_prt_legacy_file`. As well 
as to transpose the daily (wide) format to an hourly (long) format should you 
want to `daily_to_hourly`.
