# Washington-State-EV-Population-Analysis-2023-2026
This project analyzes Electric Vehicle (EV) Population Data from Washington State to understand the distribution, characteristics, and geographic patterns of registered electric vehicles. Using Python for data cleaning, exploratory data analysis (EDA), and visualization, along with Looker Studio for interactive dashboard development
Using Python for data cleaning, exploratory data analysis (EDA), and visualization, along with Looker Studio for interactive dashboard development, this project examines EV distribution by model year, manufacturer, vehicle type, electric range, geographic location, and Clean Alternative Fuel Vehicle (CAFV) eligibility.
The goal is to transform raw vehicle population data into meaningful insights through data analysis and interactive visualizations.

# Project Objectives
- Analyze the distribution of registered EVs by model year.
- Identify the most common EV manufacturers and models.
- Compare Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs).
- Examine electric range across vehicle types, manufacturers, and models.
- Identify counties and cities with the highest numbers of recorded EVs.
- Explore Clean Alternative Fuel Vehicle (CAFV) eligibility patterns.
- Analyze EV records per 1,000 residents using census-tract population estimates.
- Develop an interactive dashboard using Looker Studio to communicate key findings.

# Tools and Technologies
- Data Source: Washington State Open Data
- Python: Data Cleaning, Exploratory Data Analysis, and Visualization
- Pandas & NumPy: Data Manipulation and Numerical Analysis
- Matplotlib, Seaborn & Plotly: Data Visualization
- Looker Studio: Interactive Dashboard Development
- Google Colab: Python Development Environment
- GitHub: Project Hosting and Portfolio

# Dataset
The dataset was obtained from the official Washington State Open Data portal and is provided by the Washington State Department of Licensing.
- Official Dataset: Electric Vehicle Population Data
- Source: Washington State Open Data
- Dataset link: https://data.wa.gov/Transportation/Electric-Vehicle-Population-Data/f6w7-q2d2/about_data

- Census Population Data
Population data was obtained from the 2024 American Community Survey (ACS) 5-Year Estimates published by the U.S. Census Bureau.
Source: U.S. Census Bureau — American Community Survey

# The dataset includes information such as:
 VIN (1-10) 
 County  
 City 
 State 
 Postal Code 
 Model Year 
 Make 
 Model 
 Electric Vehicle Type 
 Clean Alternative Fuel Vehicle (CAFV) Eligibility 
 Electric Range 
 Legislative District 
 DOL Vehicle ID 
 Vehicle Location 
 Electric Utility 
 2020 GEOID 

# Dataset Files:
This repository includes:
Raw dataset ZIP file
Cleaned dataset ZIP file
Raw dataset sample in CSV format
Cleaned dataset sample in CSV format

# Methodology

# 1. Data Collection
Obtained the original Electric Vehicle Population dataset from the official Washington State Open Data portal.
 
# 2. Data Cleaning
- Inspected the dataset structure, column names, and data types.
- Checked for missing values and duplicate records.
- Handled missing values in selected columns.
- While inspecting the 790 missing values in Legislative District, found that other states' EV records data were included in the dataset, so a new dataframe was created for the Washington state EV population Analysis.
- New columns Latitude and longitude were created, and GEOID was extracted into a new column without decimal points.
- Examined duplicate DOL Vehicle ID values.
- Reviewed electric-range values, including zero values that represent unavailable or unresearched range information in the relevant records.
- Prepared the cleaned dataset for further analysis.

# 3. Exploratory Data Analysis (EDA)
Analyzed vehicle counts by model year, manufacturer, model, vehicle type, electric range, county, city, and CAFV eligibility.

# 4. Population-Adjusted Geographic Analysis
To compare EV distribution across areas with different population sizes, EV records were analyzed alongside census-tract population estimates.
The process included:
- Prepared the 11-digit census-tract GEOID for matching between datasets.
- Aggregated EV records by census tract.
- Merged the EV counts with 2024 ACS 5-year population estimates.
- Calculated EV records per 1,000 residents = (EV records in a census tract ÷ Census-tract population) × 1,000.
- Compared population-adjusted EV record counts across census tracts.

# 5. Data Visualization
Created visualizations to identify distributions, compare vehicle categories, examine electric-range patterns, and highlight geographic concentrations.

# 6. Dashboard Development
Developed an interactive Looker Studio dashboard to present key metrics, comparisons, and geographic patterns in a clear and accessible format.

# Key Findings
**- Leading manufacturer:** Tesla had the highest number of recorded EVs, with 122,573 records.
**- Most represented model year:** 2023 had the highest count, with 61,425 records.
**- Vehicle type distribution:** Battery Electric Vehicles (BEVs) accounted for 241,125 records, while Plug-in Hybrid Electric Vehicles (PHEVs) accounted for 57,791 records.
**- Geographic distribution:** King County had the highest number of recorded EVs, with 144,257 records.
**- Leading city:** Seattle had the highest city-level count, with 45,469 records.
**- Electric-range data quality:** A substantial number of records contained zero electric-range values. These were treated as unavailable or unresearched range information for the relevant analysis rather than as actual zero-mile driving ranges.
**- Population-adjusted EV distribution:** EV records per 1,000 residents were calculated at the census-tract level using 2024 ACS 5-year population estimates. The highest observed rate was approximately 465.68 EV records per 1,000 residents in Census Tract 93 in King County, based on 1,486 EV records and a population of 3,191.
These findings describe patterns in the available dataset and should not be interpreted as direct measures of annual vehicle sales or population-adjusted EV adoption rates.

# Project Deliverables:
- Raw and cleaned EV datasets
- Python data-cleaning and analysis workflow
- Exploratory data analysis and visualizations
- Population-adjusted geographic analysis
- Interactive Looker Studio dashboard
- Project documentation and findings

# Interactive Dashboard:
The **Looker Studio** dashboard presents an interactive overview of the recorded EV population in Washington State.
**Data Studio Dashboard link:* https://datastudio.google.com/reporting/41dcbf40-d324-4720-a454-9ae931db73ac

# Python Notebook:
The Python notebook documents the data-cleaning process, exploratory analysis, population-adjusted calculations, visualizations, and key findings.
**Notebook link:* 

# Limitations:
- The dataset represents recorded EV population records, not annual vehicle sales.
- Model year indicates the vehicle's model year and is not a transaction date.
- Zero electric-range values may represent unavailable or unresearched information.
- EV records per 1,000 residents are based on vehicle record counts and estimated population; they do not represent the percentage of residents who own EVs.
- Census population estimates and EV records may differ in reference period and coverage.
- Geographic comparisons depend on the accuracy of the census-tract matching and the available data.
Findings reflect the dataset snapshot used for this analysis and may change as the source dataset is updated.

# Conclusion:
This project demonstrates Python-based data cleaning, exploratory data analysis, and visualization to a real-world transportation dataset. It explores recorded EV population patterns across model years, manufacturers, vehicle types, electric ranges, and geographic locations in Washington State.
By incorporating census-tract population estimates, the project extends beyond simple vehicle counts to provide population-adjusted geographic comparisons. The interactive Looker Studio dashboard makes these findings easier to explore and interpret.
