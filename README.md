# The Impacts of Crime Rate on LGA Median House Prices in Victoria, Australia

## The Big Question
- Have crime rate affected the house prices in various LGAs within Victoria?

## Execitive Summary
- Datasets of Median House Prices and Criminal Incidents by Suburb and LGA are loaded into the workspace. After loading the datasets, they are formatted to a desired format by fixing column headers to allow for joining/merging of datasets. The dataset is also filtered to only display data from the year 2020. 
- After the joining of datasets, the process of tidying & manipulating is done by grouping the dataset by the selected variables to retrieve the total crime count within each LGA. After the creation of a new variable, it is then joined with the main dataset.
- By understanding the dataset, the various attributes and structure of the dataset were converted to their most accurate data types that will aid in future analysis. Columns that are considered redundant are removed in this step.
- The section of the data that do not conform to tidy data rules are fixed to ensure that each variable has its own column and values are recorded within rows. Variables that are supposed to be values are dealt with in an appropriate manner. As the dataset only included criminal incidents for suburbs by year, the dataset is mutated to include a new variable that displays the average criminal incidents count per quarter of the year. New variables created are converted to their rightful data structures.
- The dataset is scanned for missing values. It was determined that the missing values were caused by the lack of information/data within the Criminal Incidents by Suburb and LGA dataset. Thus, causing some suburbs to not have crime data. The decision was made to drop all the rows of missing values which make up a proportion of 1.38% of the entire dataset.
- As the distribution between the variables being investigated are bivariate, a scatterplot is used to determine the scale of possible outliers within the dataset. The scale of possible outliers and distribution of univariate outliers were also investigated here. A decision to maintain all rows was made as these possible outliers were not caused by any form of error and is critical for future analysis.
- The distributions of the quantitative variables were inspected and proper transformation techniques were applied to achieve symmetrical distributions. Various transformation techniques were used and the one that worked best was chosen to transform the skewed distribution.

## Data Collection
### Source 1:
Data Vic (https://discover.data.vic.gov.au/dataset/victorian-property-sales-report-median-house-by-suburb)

#### Description:
This dataset lists the percentage shift in median prices between quarters as well as the change over a 12-month period for Victorian houses.

#### Variables:
- Suburb - All suburbs in Victoria, Australia
- Jul-Sep 19 - Median house prices for that period
- Oct-Dec 19 - Median house prices for that period
- Jan-Mar 20 - Median house prices for that period
- Apr-Jun 20 - Median house prices for that period
- Jul-Sep 20 - Median house prices for that period
- No of Sales Jul-Sep 20 - Number of house sales for that period
- No of Sales YTD - Year to date number of house sales
- Change % Jul-Sep 19 Jul-Sep 19 - Percentage change in median house price between two periods
- Change % Apr-Jun 20 Jul-Sep 20 - Percentage change in median house price between two periods


### Source 2:
Crime Statistics Agency (https://www.crimestatistics.vic.gov.au/crime-statistics/historical-crime-data/download-data-3)

#### Description:
- There are five tables within this excel workbook. 
- The dataset of interest chosen is: Criminal Incidents by principal offence, local government area and postcode or suburb/town

#### Variables:
- Year - Displays the year when the crime was committed/recorded
- Year ending - The month when a full year is recorded (September for this dataset)
- Local Government Area - The LGA where the crime was committed/recorded
- Postcode - The postcode of the suburb where the crime was committed/recorded
- Suburb/Town Name - The suburb where the crime was committed/recorded
- Offence Division - General category of the crime committed/recorded
- Offence Subdivision - Offence division specific category of crime committed/recorded
- Offence Subgroup - Subgroup of crime committed/recorded (Finest granularity of crime category)
- Incidents Recorded - Number of crimes recorded

## Tools and Technologies
Scripting language: R
Editor: RStudio
Format: RMarkdown
Packages: kableExtra, magrittr, dplyr, tidyr, readr, readxl, openxlsx, ggplot2, tools, forecast