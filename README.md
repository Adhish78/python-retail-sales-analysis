# Online Retail Sales Analysis



## Overview
This project explores and analyzes sales data from an online retail store using Python. It covers various aspects such as data cleaning, exploratory data analysis (EDA), feature engineering, and time series forecasting using the Prophet library. The analysis aims to derive insights into sales trends, customer behavior, and key performance indicators (KPIs) to inform business strategies and decision-making.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Analysis Steps](#analysis-steps)
  - [Data Loading and Inspection](#data-loading-and-inspection)
  - [Data Cleaning](#data-cleaning)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Feature Engineering](#feature-engineering)
  - [Key Performance Indicators (KPIs)](#key-performance-indicators-kpis)
  - [Time Series Forecasting with Prophet](#time-series-forecasting-with-prophet)
- [Key Findings](#key-findings)
- [Dependencies](#dependencies)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Introduction
In this project, we delve into an online retail dataset to understand sales patterns over time, customer demographics, and seasonal trends. The analysis includes visualizations and metrics to uncover insights that can aid in strategic decision-making for business growth.

## Dataset
The dataset used in this project is the [Online Retail II dataset](https://doi.org/10.24432/C5CG6D) from the UCI Machine Learning Repository. This dataset contains transactional records from an online retail store over a period of two years (2009-2011). Each transaction includes attributes such as Invoice ID, Stock Code, Description, Quantity, Price, Customer ID, Country, and Invoice Date.

## Analysis Steps
### Data Loading and Inspection
1. **Data Loading**: The dataset is loaded using pandas from an Excel file.
2. **Inspection**: Basic information about the dataset is obtained, such as data types, number of entries, and presence of missing values.

### Data Cleaning
1. **Handling Missing Values**: Rows with missing values are dropped to ensure data quality.
2. **Data Type Conversion**: Data types are converted to more memory-efficient formats (e.g., categorical variables).
3. **Outlier Removal**: Outliers in Quantity and Price columns are removed using the interquartile range (IQR) method.

### Exploratory Data Analysis (EDA)
1. **Distribution Analysis**: Visualizations such as histograms and box plots are used to analyze the distribution of Quantity and Price.
2. **Time-Based Analysis**: Trends in transaction counts over time (by day) are plotted to identify seasonal patterns.
3. **Customer Behavior**: Distribution of transactions by day of the week, month, quarter, hour, and year is analyzed to understand customer engagement.

### Feature Engineering
1. **Date-Time Features**: New features such as DayOfWeek, Month, Quarter, Hour, Year, YearMonth, and YearQuarter are extracted from the InvoiceDate column for deeper analysis and modeling.

### Key Performance Indicators (KPIs)
1. **Total Revenue**: Calculated as the sum of Quantity * Price, analyzed over Year-Month and Year-Quarter.
2. **Number of Orders**: Count of unique Invoice IDs, analyzed over Year-Month and Year-Quarter.
3. **Average Purchase Frequency**: Ratio of Number of Orders to Number of Unique Customers, analyzed over Year-Month and Year-Quarter.
4. **Average Revenue per User (ARPU)**: Ratio of Total Revenue to Number of Unique Customers, analyzed over Year-Month and Year-Quarter.
5. **Average Order Value (AOV)**: Ratio of Total Revenue to Number of Orders, analyzed over Year-Month and Year-Quarter.
6. **Unique Customer Count**: Count of unique Customer IDs, analyzed over Year-Month and Year-Quarter.
7. **Total Quantity of Products Sold**: Sum of Quantity sold, analyzed over Year-Month and Year-Quarter.
8. **Unique Orders per Country**: Count of unique Invoice IDs per Country, analyzed to understand sales distribution.

### Time Series Forecasting with Prophet
1. **Daily Revenue Forecast**: Prophet library is used to forecast daily revenue trends, including model initialization, fitting, future predictions, and visualization of forecasted results.
2. **Monthly Revenue Forecast**: Monthly revenue trends are forecasted using Prophet, including data preparation, model fitting, future predictions, and visualization.

## Key Findings
- Seasonal trends in sales based on month, quarter, and year.
- Peak transaction times by day of the week and hour.
- Revenue trends and forecasts highlighting growth opportunities.
- Customer behavior insights such as purchase frequency and spending patterns.

## Dependencies
The project requires the following Python libraries:
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- prophet


## License

This project is licensed under the MIT License - see the [LICENSE]([link](https://github.com/Adhish78/python-retail-sales-analysis/blob/main/LICENSE)) file for details.


## Acknowledgments
- Dataset: Chen, Daqing. (2019). Online Retail II. UCI Machine Learning Repository. https://doi.org/10.24432/C5CG6D
- Special thanks to the Python community for developing and maintaining the open-source libraries used in this project.
