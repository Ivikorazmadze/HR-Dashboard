# For-HR
---
## Overview
- Insights of company's employees distribution in important aspects.
- Provide insights into retrenchment, promotion, and necessary actions to be taken.
- This dashboard is meant for the HR department’s daily use
## Data Source
Data source was used from [Kaggle Link](https://www.kaggle.com/datasets/rishikeshkonapure/hr-analytics-prediction).
## Explorator Data Analysis
EDA involved exploring the data to answer the following questions.
-Total employees distribution by gender, On Service, Retrenchment, Distance, Promotion, Job level and Role.
## List of DAX used for analysis

```DAX
Total Employees = COUNTROWS('HR Analytics Data')
```
```DAX
Due for Promotion = IF(ISBLANK(CALCULATE([Total Employees],'HR Analytics Data'[Promotion Status] = "Due For Promotion")),0,
CALCULATE([Total Employees],'HR Analytics Data'[Promotion Status] = "Due For Promotion"))
```
```DAX
Female = CALCULATE([Total Employees],'HR Analytics Data'[Gender]="Female")
```
```DAX
Male = CALCULATE([Total Employees],'HR Analytics Data'[Gender]="male")
```
```DAX
On Service = CALCULATE([Total Employees],'HR Analytics Data'[Retrenchment status] = "On Service")
```
```DAX
Will be Retrenched = [Total Employees] - [On Service]
```
```DAX
Not Due = CALCULATE([Total Employees],'HR Analytics Data'[Promotion Status] = "Not Due")
```





