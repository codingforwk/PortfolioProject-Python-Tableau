# London Bike Data Cleaning and Transformation

## 📄 Project Overview

This project loads a raw CSV file containing bike-sharing data for London, performs data cleaning and transformation steps, and saves the final cleaned dataset into an Excel file (`london_bikes_New.xlsx`).

The main goals are:
- Improve column naming for clarity
- Normalize humidity values
- Map numeric codes to descriptive weather and season names
- Export the cleaned dataset for further analysis or visualization

---

## 📂 Dataset Description

**Input file**:  
`london_merged.csv` (downloaded manually)

**Raw Columns**:
- `timestamp`: Timestamp of the record
- `cnt`: Number of bike shares
- `t1`: Actual temperature (°C)
- `t2`: Feels-like temperature (°C)
- `hum`: Humidity (%)
- `wind_speed`: Wind speed (km/h)
- `weather_code`: Numeric weather code
- `is_holiday`: 1 if holiday, else 0
- `is_weekend`: 1 if weekend, else 0
- `season`: Season as a numeric code (0-3)

---

## 🔧 Processing Steps

1. **Load Data**  
   - Read the CSV file into a pandas DataFrame.

2. **Rename Columns**  
   - Improve readability by renaming columns:
     - Example: `cnt` ➔ `count`, `t1` ➔ `temp_real_C`, etc.

3. **Normalize Humidity**  
   - Convert `humidity_percent` from percentage (0–100) to a fraction (0–1).

4. **Map Categorical Codes**  
   - Replace `season` numeric codes with season names (`Spring`, `Summer`, `Fall`, `Winter`).
   - Replace `weather` numeric codes with weather descriptions (`Clear`, `Rain`, `Snowfall`, etc.).

5. **Save the Cleaned Data**  
   - Export the cleaned DataFrame to an Excel file: `london_bikes_New.xlsx` under a sheet named `Data`.

## 📊  Dashboard
