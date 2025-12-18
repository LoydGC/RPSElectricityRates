Project Overview
This analysis explores the relationship between state-level Renewable Portfolio Standards (RPS) policies and electricity prices in the United States from 2010-2023. Using data from multiple sources including the U.S. Energy Information Administration (EIA), Bureau of Economic Analysis (BEA), and U.S. Census Bureau, I investigate whether RPS mandates affect electricity costs for consumers.


Research Questions:

Do states with active RPS policies exhibit different electricity price distributions compared to states without RPS?

Is monthly electricity price volatility higher in state-years with RPS policies compared to those without?

How does the relationship between RPS targets and electricity prices differ across economic wealth levels (GDP per capita)?

Have electricity price trends diverged over time between RPS and non-RPS observations when controlling for state economic wealth?

How do electricity consumption patterns and costs vary across sectors (residential, commercial, industrial) in states with and without RPS policies?

Data Sources
This analysis combines five data sources to examine electricity prices and renewable energy policy across U.S. states from 2010-2023:

1. Electricity Market Retail Sales Data (EIA API)
Monthly retail electricity statistics including price (cents/kWh), sales volume, revenue, and customer counts for all 50 states plus D.C., broken down by sector (residential, commercial, industrial, transportation).

3. Renewable Portfolio Standards (RPS) Policy Data (Lawrence Berkeley National Laboratory)
State-level requirements for renewable energy generation, showing which states have RPS policies and their target percentages by year. I created a binary indicator for whether each state had an active RPS policy.

4. Economic Data (Bureau of Economic Analysis)
State GDP figures used to calculate GDP per capita, which serves as a proxy for state wealth and cost of living.

5. Population Data (U.S. Census)
Annual state population estimates from the American Community Survey 5-Year Estimates used to calculate GDP per capita.

6. CPI Data (Consumer Price Index Python Library)
Consumer Price Index (CPI) data to adjust electricity prices for inflation, ensuring comparability over time.

Final Dataset:
The merged dataset contains 42,840 observations, where each row represents a specific state-month-sector combination with electricity market metrics, RPS policy status, and economic context. This structure enables comparison of electricity prices and consumption patterns between states with and without renewable energy mandates while accounting for economic differences. Due to a mismatch in available years after 2023 with some of the datasets, I decided to only use 2010-2023 for consistency across all data sources and to prevent missing data issues.

Key Variables
Price: Average retail electricity price (cents/kWh) by state, sector, and month
RPS Binary: Indicator for whether a state has an active RPS policy in a given year
RPS Target: Percentage of electricity generation required from renewable sources
GDP per Capita: State economic output per person (proxy for wealth/cost of living)
Sector: Residential, commercial, industrial, or transportation
Methodology
Data collection and cleaning from multiple APIs and Excel files
Construction of state-month panel dataset (2010-2023)
Exploratory data analysis through visualizations and summary statistics
