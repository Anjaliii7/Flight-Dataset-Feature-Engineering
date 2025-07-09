
# ✈️ Flight Price Prediction - EDA & Feature Engineering 

Welcome to my Flight Price Prediction project!  
In this notebook, I performed detailed **Exploratory Data Analysis (EDA)** and extensive **Feature Engineering** on a flight dataset, preparing it for machine learning model development.

---

## 📂 Dataset 

| **Variable**  | **Description**                                                             |
| :------------ | :-------------------------------------------------------------------------- |
| `date`        | Date of the flight journey (usually in `dd-mm-yyyy` or `yyyy-mm-dd` format) |
| `airline`     | Name of the airline operating the flight (e.g., Indigo, SpiceJet)           |
| `ch_code`     | Airline flight code prefix (e.g., AI, SG)                                   |
| `num_code`    | Numeric flight number/code (e.g., 457, 8256)                                |
| `dep_time`    | Scheduled departure time of the flight (in `HH:MM` format)                  |
| `from`        | Departure city/airport                                                      |
| `duration`    | Total duration of the flight (e.g., `2h 50m`)                               |
| `stop`        | Number of stops in the journey (Non-stop, 1-stop, 2-stop, etc.)             |
| `arr_time`    | Scheduled arrival time of the flight (in `HH:MM` format)                    |
| `destination` | Destination city/airport                                                    |
| `price`       | Ticket price for the flight (in ₹ Rupees, sometimes with commas)            |

## Objectives  

- Clean and preprocess the raw dataset  
- Handle missing values and inconsistent entries  
- Perform EDA using **visualizations and descriptive statistics**  
- Apply **Feature Engineering** techniques:
  - Date-Time feature extraction (year, month, day, hours, minutes)
  - Mapping categorical columns (`Stop`) to numerical
  - One-Hot Encoding for categorical features (`Airline`, `Source`, `Destination`, `Ch_Code`, etc.)
  - Converting price from string to numeric
  - Handling constant and redundant columns

---

## ❗ Problems Tackled  

- **Handling Date-Time Features:** Extracting `year`, `month`, `day`, `hour`, and `minute` from raw date and time strings  
- **One-Hot Encoding:** Converting multiple categorical columns like `Airline`, `Ch_Code`, etc. into numeric one-hot encoded variables  
- **Mapping Stops:** Cleaning and mapping `Stop` feature values (with extra spaces and different naming patterns) into numeric codes  
- **Generating Correlation Heatmap:** Identifying and resolving issues where certain columns like `Year` were missing or had constant values causing `NaN` in correlation matrices  
- **Managing Price Format:** Converting flight price values from string with commas (e.g., '5,953') to proper numeric data type  
- **Dealing with Congested Heatmaps:** Adjusting figure size, label rotation, and layout to handle large numbers of columns from one-hot encoding  

---

## 📌 Key Insights  

- Majority of the flights in the dataset have **1 stop**  
- Price distribution is highly skewed with notable outliers  
- Certain date-time features like month and departure/arrival hours impact price trends  
- Variable "year" contains only 1 value for all columns , making its variance as 0 , so it does not show any correlation in heatmap
---
