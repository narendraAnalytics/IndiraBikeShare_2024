# Indira Bikeshare 2024

![BikeShare Banner](Images_BikeShare_Images/BikeShareBannerImage.jpg)

## Overview
This project analyzes bikeshare data to understand user behavior, optimize pricing strategies, and improve station efficiency. The data includes bikeshare usage, user demographics, and financial performance from multiple stations.

## Features
- **Data Cleaning:** Ensured data quality by handling missing values, correcting inconsistencies, and formatting columns.
- **Preprocessing:** Applied SQL queries for feature engineering, normalizing data, and generating insights for analysis.
- **Feature Engineering:** Extracted key features such as trip duration, user type analysis, and peak hours.
- **Power BI Dashboard:** An interactive dashboard was created to visualize key metrics and insights. The dashboard provides a comprehensive view of bikeshare data and financial performance.

---

### Power BI Dashboard
Access the interactive dashboard here: [Indira Bikeshare Power BI Dashboard](<Insert_Power_BI_Dashboard_Link_Here>)

---

## Datasets and Column Descriptions

### **BikeShare Data**
This dataset contains information about bikeshare usage, including user behavior and trip details.

| Column Name          | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| `Date`               | The date of the trip.                                                      |
| `Time`               | The time the trip started.                                                 |
| `Year`               | The year when the trip occurred.                                           |
| `Month`              | The month when the trip occurred.                                          |
| `Hour`               | The hour when the trip occurred.                                           |
| `Holiday`            | Indicates whether the trip occurred on a holiday (`Yes` or `No`).          |
| `Working Day`        | Indicates whether it was a working day (`Yes` or `No`).                    |
| `Weekday`            | The day of the week (e.g., Monday, Tuesday).                               |
| `Temperature`        | The temperature (in degrees Celsius) during the trip.                     |
| `Station ID`         | Unique identifier for the station where the trip started.                  |
| `User ID`            | Unique identifier for the user.                                            |
| `User Age`           | The age of the user.                                                       |
| `User Gender`        | The gender of the user (`Male` or `Female`).                               |
| `Trip Duration`      | The duration of the trip (in minutes).                                     |
| `Trip Start Time`    | The exact time the trip started.                                           |
| `Trip End Time`      | The exact time the trip ended.                                             |
| `Season`             | The season when the trip occurred (e.g., Winter, Summer).                 |
| `Weather Conditions` | Describes the weather during the trip (e.g., Cold, Sunny).                |
| `Rider Type`         | Indicates whether the rider is a subscriber or casual user.               |
| `Bike Type`          | The type of bike used (e.g., Premium Bike, Standard Bike, Electric Bike).  |

---

### **BikeShare Financial Data**
This dataset contains financial details for bikeshare stations.

| Column Name          | Description                                            |
|-----------------------|--------------------------------------------------------|
| `Station ID`         | Unique identifier for the station.                     |
| `Station Location`   | The location of the station.                           |
| `Year`               | The year of financial data.                            |
| `COGS`               | Cost of Goods Sold (in local currency).                |
| `Price per Minute`   | The price charged per minute of bike usage.            |

---

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
