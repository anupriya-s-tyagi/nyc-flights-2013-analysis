# NYC Flights 2013: Exploratory Analysis and Business Questions

Exploratory data analysis of every flight that left New York City (EWR, JFK, LGA) in 2013, using the public `nycflights13` dataset (336,776 flights across 5 related tables), with Python and pandas.

## What this covers
1. **EDA and data cleaning** (`01_EDA.ipynb`): data quality checks on all five tables, missing values, outliers (including an impossible 1,048 mph wind reading and bad airport coordinates in the source data), and feature preparation.
2. **Cross-table joins** (`02_cross_table_joins.ipynb`): flights joined with airlines and airports to answer questions about carriers, hubs and destination time zones.
3. **Business questions** (`03_business_questions.ipynb`): 15 questions framed as an operations team or executive would ask them, from market share to "where should the CEO focus to cut delays by 10%?"

## Key findings
- United is the largest carrier (17.4% of departures); no single airline dominates all three airports.
- Frontier, ExpressJet, AirTran and Mesa rank among the worst for both departure and arrival delay, though Frontier, Mesa and SkyWest have small samples, so their rankings need caution.
- Newark (EWR) is the busiest origin and has the worst average departure delay (15.1 min). 9 of the 10 worst-delayed routes start there, which points to an airport-level issue rather than a route-level one.
- JFK to LAX is the busiest route.
- About 2.5% of flights were cancelled, with February the worst month (5%).

## Data quality notes
- 8,255 flights have no departure data (cancelled). A further ~1,175 flights departed but have no arrival delay recorded.
- One wind-speed reading of 1,048 mph was removed as a sensor error. Wind gust data was ~80% missing and was dropped.
- One airport (EEN) has swapped latitude/longitude in the source data and was excluded from the northernmost-airport analysis.

## Tools
Python, pandas, NumPy, seaborn, matplotlib, Jupyter.

## How to run
pip install pandas numpy matplotlib seaborn nycflights13 jupyter

Then open the notebooks in order. No data download is needed, because the dataset comes with the `nycflights13` package.
pip install pandas numpy matplotlib seaborn nycflights13 jupyter

Then open the notebooks in order. No data download is needed, because the dataset comes with the `nycflights13` package.
