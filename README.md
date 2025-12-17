# UK-Balancing-Market-Price-Forecasting-The-Influence-of-Generator-Availability

Remit Data Analysis File:
- Reads three CSV files: 1. REMIT_2021_2024.csv (the raw remit data) 2. Dates_SP_2021_2024,csv (half hour settlement periods) 3. BMUFuelType.csv (BMU fuel type definitions to match the generators to)
- The REMIT_2021_2024.csv is too large a file to share on Github, have shared on emaiil
- Script cleans the data and aggregates the data onto a half hour scale for each unit, then performs exploratory analysis

System Price Forecasting- SHAP Feature Analysis:
- Reads five CSV files: 1. Final_Dataset_Forward_Forecasts_2021_2024.csv (df with the system price we are forecasting) 2. REMIT_Unavailable_Capacity_Percentage_By_FuelType_And_Availability_Type.csv (fuel type dataset, we are not interested in this data) 3. Individual_Unit_Capacity.csv (individual unit capacity outage data for planned and unplanned combined) 4. Individual_Unit_Capacity_Planned.csv (individual unit capacity data for planned outages) 5. Individual_Unit_Capacity_Unplanned.csv (individual unit capacity data for unplanned outages)
- All files are too big to be shared over Github, have shared over email
- XGBoost regression model to evaluate impact of different generators on system price, models are optimised using optuna and SHAP values are averaged across 10 model runs, with final SHAP value an average across all runs 
