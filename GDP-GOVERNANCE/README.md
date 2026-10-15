# Governance and Economic Outcomes: A Cross-country Analysis 

## Overview

This project examines the relationship between the quality of goverance and the economic outcomes across countries using data from the World Bank and World World Goverance Indicators. This project combines two datasets to produce a country-year one to do a preliminary emperical analysis using Python. 

## Question

Is better governance associated with a higher GDP per capita? 

Following are the dimensions of governance analysed:

-Control of Corruption: Extent to which public power is exercised for private gain. 

-Government Effectiveness: Reflects the quality of civil and public services and the policy implementation. 

-Rule of Law: Reflects the quality of contract enforcement, the police, property rights, the courts, and adherence to rules of society. 

## Data Sources 

### World Bank Indicators 
-GDP Per Capita (constant 2015 US$)
-GDP Growth (annual %)

### World Governance Indicators 
-Control of Corruption
-Government Effectiveness 
-Rule of Law

## Methodology 

1. Load in the datasets. 
2. Identify the relevant indicators. 
3. Clean and reshape the datasets. 
4. Merge the datasets by country codes and year. 
5. Perform a regression of the log of GDP Per Capita on the governance indicators. 
6. Plot the regression of the log of GDP Per Capita on each governance indicator individually. 

## Tools and Libraries 

-Python
-pandas: Data cleaning, reshaping, and merging
-numpy
-matplotlib: Data visualization 
-statsmodels: OLS Regression 
-Jupyter Notebook 

## Results 

### Regression Results 

The OLS estimates the regression of the log of GDP Per Capita on Control of Corruption, Governemnt Effectiveness, and Rule of Law. The R-squared value is 0.760 while the adjusted R-squared value is 0.752 implying that around 75% of the variation in the dependent variable is explained by the explanatory variables. We have the coefficients as: 

-Control of Corruption: The estimated value is 2.3856 with a p-value of 0.000 implying significance. 
-Government Effectiveness: The value is 0.0740 with a p-value of 0.791 which is insignificant even at 10% level of significance. 
-Rule of Law: The value is -0.9577 with a p-value of 0.001 implying significance. 

### Visual Results 

We see that all of the individual regressions produce a regression line with a positive slope implying postive individual associations of each regressor with the log of GDP Per Capita. 

### Key Takeaway 

While each of them share a positive relationship with GDP Per Capita individually, we see that in the overall regression, rule of law is negatively associated with log of GDP Per Capita. The high correlations among the regressors, as shown by the correlation matrix, help in explaining such a "sign reversal." However, despite the crude nature of the analysis, we do notice some degree of positive effect of good governance on economic performance.  

## Limitations 

This is only a preliminary analysis, hence the results shouldn't be interpreted as causal. The governance indicators are highly correlated with one another. The analysis doesn't, in its OLS form, adress reverse causality, omitted variables, or unobserved country-specific charactersitics. 

## Conclusion 

This projects demonstrates a workflow for merging datasets, using them for OLS, and plotting various regression results to adress various economic questions. It, thus, serves as a starting point for further investigation into the relationship between the performance of institutions and economic outcomes.  





