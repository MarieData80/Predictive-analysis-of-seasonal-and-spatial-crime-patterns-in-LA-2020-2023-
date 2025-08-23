#Data Engineering 

![Fig 01](../images/Fig%2001.png)

The data engineering followed a simplified Extract Transform Load process (A simplified ETL model 2(Reis, J. and Housley, M. (2022))
The data preprocessing had over 900,000 lines of data in a CSV file imported into Excel /Power Query for transformation 
Data type was assigned focusing on date / time fields with calendar data, numerical codes for the division number and decimal for location coordinates.   
As only time series and spatial analysis data was required unnecessary or duplicate data was removed.    

![Fig 02](../images/Fig02.png)

# Iteration 
Cleaning initially tool place in Python / Gemini. The data was returned efficiently but was missing nearly 400’000 lines. The decision was made to restart with Microsoft products. This took longer but there was a clear understanding of how the data was being transformed.   

Renaming of columns ensured analysis could move efficiently. Date and time was formatted and placed in separate columns.  
Further cleaning took place to highlight any errors before moving across to the Load process.  
A MATCH test was run between the DR_NO column and the AREA_NO column highlighting discrepancies. The decision was made to use the AREA_NO as the correct data source as the DR_NO was potentially inputting human error 
Imputing was actioned on some blank cells / missing data for AREA_NO. This could be actioned by referring to the data in cell DR_NO. 
267 lines of data where cleaned 36 lines of data were removed due to insufficient or incorrect data entry. The number was small enough to not affect the overall reading of the data set. 

![Fig 03](../images/Fig03.png)

Key feature engineering steps in the data included extraction of year, month, day from date. Time blocks were also added to enable time series analysis.

Standardisation or normalisation were not needed as the analysis is focused on crime counts not scaled variables for predictive modelling. 
