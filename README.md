# What-Drives-Youth-Unemployment-in-Nigeria-An-Economic-Social-Indicators-Analysis-2000-2024-
An end-to-end data analytics project investigating the relationship between youth unemployment and key economic and development indicators in Nigeria using the World Bank API, Python, statistical analysis, and Power BI.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<img width="2752" height="1536" alt="Project Image" src="https://github.com/user-attachments/assets/c90f7121-22c2-4c54-b9cb-83556b74a4b0" />

## Project Overview

Youth unemployment remains an important economic and social challenge in Nigeria. However, unemployment does not exist in isolation, it can be influenced by broader economic conditions, investment, and infrastructure development.

This project investigates the relationship between Youth Unemployment and selected economic and development indicators in Nigeria between 2000 and 2024.

The analysis combines:

 API data collection  
 Python data analysis  
 Exploratory Data Analysis  
 Correlation analysis  
 Multiple Linear Regression  
 Regression diagnostics  
 HAC robust regression  
 Power BI dashboard development.

 ## Research Question

What economic and social indicators are associated with youth unemployment in Nigeria?  

The project investigates the relationship between youth unemployment and:
GDP Growth  
Inflation  
Foreign Direct Investment (FDI)  
Internet Usage  
Electricity Access. 


## Executive Summary

Using 25 years of World Bank data (2000–2024), this analysis explored the relationship between youth unemployment and selected economic and development indicators in Nigeria.

### Key findings:

i. GDP Growth showed a statistically significant negative association with youth unemployment.

ii. Inflation also showed a statistically significant negative association with youth unemployment in the final model.

iii. Foreign Direct Investment (FDI) was not statistically significant in the final regression model.

iv. Electricity Access was not statistically significant in the final regression model.

v. The final regression model explained approximately 63.8% of the variation in youth unemployment.


## Key Results at a Glance

| Metric                               |            Result | What It Means                                                          |
| ------------------------------------ | ----------------: | ---------------------------------------------------------------------- |
| **R²**                            | **0.638 (63.8%)** | The final model explains 63.8% of the variation in youth unemployment  |
| **Adjusted R²**                   | **0.565 (56.5%)** | Model performance adjusted for the number of predictors                |
| **Observations**                  |            **25** | Annual data covering 2000–2024                                         |
| **GDP Growth Coefficient**        |       **−0.2378** | Statistically significant negative association with youth unemployment |
| **Inflation Coefficient**         |       **−0.1174** | Statistically significant negative association with youth unemployment |
| **FDI Coefficient**               |       **−0.1807** | Negative association, but not statistically significant                |
| **Electricity Access Coefficient** |       **−0.0661** | Negative association, but not statistically significant                |
| **Internet Usage Correlation**    |        **−0.041** | Little to no linear relationship with youth unemployment               |
| **Model p-value**                 |      **0.000231** | The overall regression model is statistically significant              |


## Power BI Dashboard

The Power BI dashboard provides an interactive overview of youth unemployment and key economic and development indicators in Nigeria.

Dashboard features include:
KPI cards for key indicators  
Year-over-Year comparisons  
Youth unemployment trend analysis  
Economic and social indicator trends

<img width="978" height="551" alt="projectimage2" src="https://github.com/user-attachments/assets/6037b059-79ce-4b5a-b01c-9e40b1588aae" />


## Analytical Workflow

World Bank API
      │
      ▼
Data Collection
      │
      ▼
Data Cleaning & Preparation
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Correlation Analysis
      │
      ▼
OLS Regression
      │
      ▼
Multicollinearity Testing (VIF)
      │
      ▼
Regression Diagnostics
      │
      ▼
HAC Robust Regression
      │
      ▼
Power BI Dashboard


## Data Source

The data used in this project was obtained from the World Bank API.

The analysis covers Nigeria from: 2000–2024.

## Indicators Used
| Indicator | Description |
|---|---|
| Youth Unemployment | Youth unemployment rate |
| GDP Growth | Annual GDP growth rate |
| Inflation | Annual inflation rate |
| FDI | Foreign Direct Investment as a percentage of GDP |
| Internet Usage | Percentage of individuals using the internet |
| Electricity Access | Percentage of the total population with access to electricity |


## Tools & Technologies
| Tool | Purpose |
|---|---|
| **Python** | Data analysis and statistical modeling |
| **Pandas** | Data cleaning and manipulation |
| **Requests** | API data extraction |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical visualization |
| **Statsmodels** | Regression analysis and diagnostics |
| **World Bank API** | Data source |
| **Power BI** | Interactive dashboard and storytelling |
| **Jupyter Notebook** | Analysis documentation |

## Data Collection & Preparation
The data was collected programmatically using the World Bank API.

The workflow included:

Retrieving indicator data for Nigeria  
Combining multiple indicators into a single dataset  
Handling missing values  
Checking data types  
Removing incomplete observations  
Excluding 2025 because complete data was unavailable.

The final dataset contained: 25 observations × 7 variables
covering the period: 2000–2024.

## Exploratory Data Analysis

Exploratory Data Analysis was conducted to understand:

The distribution of the variables  
Historical trends  
Relationships between indicators    
Potential outliers  
Correlation patterns.  

The analysis included:

Summary statistics  
Line charts  
Scatter plots  
Correlation analysis. 


## Correlation Analysis

The correlation analysis examined the linear relationship between youth unemployment and the selected indicators.

| Indicator | Correlation |
|---|---:|
| GDP Growth | **−0.532** |
| Inflation | **−0.530** |
| FDI | **−0.197** |
| Internet Usage | **−0.041** |
| Electricity Access | **−0.073** |

GDP Growth and Inflation showed the strongest correlations with youth unemployment among the selected indicators.

However, Correlation does not imply causation. The relationships were therefore investigated further using multiple regression analysis.

## Regression Analysis

A multiple linear regression model was used to examine the relationship between youth unemployment and the selected explanatory variables.

The final model included:
| Variable | Coefficient | p-value | Statistical Significance |
|---|---:|---:|---|
| GDP Growth | **−0.2378** | **< 0.001** | Significant |
| Inflation | **−0.1174** | **< 0.001** | Significant |
| FDI | **−0.1807** | 0.554 | Not Significant |
| Electricity Access | **−0.0661** | 0.150 | Not Significant |

The model explains approximately:

63.8% of the variation in youth unemployment within the dataset.

##  Multicollinearity Testing

Variance Inflation Factor (VIF) analysis was performed to identify potential multicollinearity among the explanatory variables.

Final VIF Results
| Variable | VIF |
|---|---:|
| GDP Growth | **3.86** |
| Inflation | **8.41** |
| FDI | **5.21** |
| Electricity Access | **11.30** |

The VIF analysis was used as part of the model refinement process to assess relationships among the explanatory variables.

## Regression Diagnostics

Regression diagnostics were performed to evaluate important assumptions of the model.

The analysis included:

i. Residual Analysis : Residual plots were examined to assess the distribution and pattern of model errors.

ii. Heteroscedasticity Testing : A Breusch-Pagan test was performed to investigate whether the variance of the residuals was constant.

iii. Autocorrelation Testing : The Durbin-Watson statistic was examined for potential autocorrelation. Durbin-Watson Statistic: 1.109

Because diagnostic testing suggested potential issues affecting the reliability of conventional standard errors, the final model used: Heteroscedasticity and Autocorrelation Consistent (HAC) standard errors. This provides more robust statistical inference in the presence of heteroscedasticity and autocorrelation.

## Key Insights
i. GDP Growth had a statistically significant negative association with youth unemployment.
Coefficient: −0.2378
This indicates that, within the fitted model and dataset, higher GDP growth was associated with lower youth unemployment.

ii. Inflation also showed a statistically significant negative association with youth unemployment.
Coefficient: −0.1174
This relationship should be interpreted within the context of the model and should not be interpreted as proof of causation.

iii. Foreign Direct Investment had a negative coefficient but was not statistically significant in the final model.
p-value: 0.554
This means the analysis did not provide sufficient statistical evidence of a significant association between FDI and youth unemployment in this model.

iv. Electricity Access was also not statistically significant in the final regression model.
p-value: 0.150

## Important Limitations

This analysis has several limitations:

The dataset contains only 25 annual observations
The analysis examines associations, not causation
Other factors influencing youth unemployment were not included in the model
Annual data may not capture shorter-term economic changes
Statistical relationships may be affected by omitted variables

Therefore, the results should be interpreted as:
Evidence of statistical relationships within the selected dataset—not proof of causal relationships.

