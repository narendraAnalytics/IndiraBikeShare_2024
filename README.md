# Indira Bikeshare 2024

![BikeShare Banner](Images_BikeShare_Images/BikeShareBannerImage.jpg)

## Overview
This project analyzes bikeshare data to understand user behavior, optimize pricing strategies, and improve station efficiency. The data includes bikeshare usage, user demographics, and financial performance from multiple stations.

## Features
- **Data Cleaning:** Ensured data quality by handling missing values, correcting inconsistencies, and formatting columns.
- **Preprocessing:** Applied SQL queries for feature engineering, normalizing data, and generating insights for analysis.
- **Feature Engineering:** Extracted key features such as trip duration, user type analysis, and peak hours.

## Tools and Technologies
- **SQL:** Used for data cleaning and preprocessing.
- **Python (Pandas):** Analyzed and visualized data.

## SQL Queries
### Data Cleaning
```sql
UPDATE bikeshare_data
SET temperature = ROUND(temperature, 1)
WHERE temperature IS NOT NULL;

DELETE FROM bikeshare_data
WHERE trip_duration <= 0;
