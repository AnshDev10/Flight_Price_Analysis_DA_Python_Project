# ✈️ Flight Price Analysis (India - 2019)

### 📌 Overview

This project analyzes domestic flight ticket prices in India using a dataset of **10,683 rows and 11 columns**. The objective is to understand how different factors such as airline, route, number of stops, duration, and timing influence ticket prices.

The analysis was performed using Python in Google Colab.


## 📂 Dataset Details

* **Rows:** 10,683
* **Columns:** 11
* **Target Variable:** `Price`

### 📊 Price Summary

* Mean: ₹9,087
* Median: ₹8,372
* Min: ₹1,759
* Max: ₹79,512
* Std Dev: ₹4,611

### ⚠️ Missing Values

* `Route` → 1 missing value
* `Total_Stops` → 1 missing value

✔ Missing values were handled using **mode imputation**


## ⚙️ Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Google Colab


## 🧹 Data Cleaning & Preprocessing

### ✔ Handling Missing Values

* Filled missing values in `Route` and `Total_Stops` using mode

### ✔ String Operations

* Used `.strip()` to remove extra spaces
* Used `.replace()` to:

  * Convert `Total_Stops` into numerical values
  * Clean `Duration` column by removing "h" and "m"


## 🔧 Feature Engineering

### 📅 Date Features

From `Date_of_Journey`:

* Journey Day
* Journey Month


### ⏰ Time Features

From `Dep_Time`:

* Dep Hour
* Dep Minute

From `Arrival_Time`:

* Arrival Hour
* Arrival Minute


### ⏳ Duration Features

* Duration Hours
* Duration Minutes


### 🛑 Stops Conversion

* Converted categorical stop values into numeric format


### 🗑️ Columns Dropped

* `Date_of_Journey`
* `Dep_Time`
* `Arrival_Time`
* `Duration`
* `Route`
* `Additional_Info`


## 🔍 Exploratory Data Analysis (EDA)

The analysis focused on group-based aggregations and comparisons:

* Airline-wise average price analysis
* Route-wise price comparison
* Number of stops vs average price
* Source-wise flight distribution
* Month-wise average price trends
* Departure time comparison across airlines
* Duration comparison across airlines


## 📊 Key Insights

### ✈️ Airline Insights

* Jet Airways has the highest average ticket price
* It also has the highest number of flights
* Trujet has the least number of records


### 🛫 Route Insights

* Delhi → Cochin route has the highest average ticket price


### 🔁 Stops vs Price

* 4-stop flights have the highest average prices
* Non-stop flights have the lowest prices
* Increase in stops generally leads to higher prices


### 🏙️ Source Insights

* Delhi is the busiest source airport
* Chennai has the lowest number of flights


### 📅 Monthly Trends

* March has the highest average prices
* April has the lowest average prices


### ⏰ Departure Time Trends

* Air Asia has the latest average departure time (~2 PM)
* Multiple carriers Premium Economy has the earliest (~8 AM)


### ⏳ Duration Insights

* Air India and Jet Airways have longer average durations
* SpiceJet and Vistara Premium Economy have shorter durations


## 📁 Project Structure

flight_price.xlsx
Flight_Price_Analysis.ipynb
README.md


## 🧠 Conclusion

This project demonstrates how multiple factors such as airline choice, route, number of stops, and travel timing collectively influence flight ticket pricing. By cleaning and transforming raw data into structured features, it became possible to uncover clear pricing patterns using simple yet effective analytical techniques.

The analysis shows that pricing is not driven by a single variable but by a combination of operational and demand-based factors. Airlines like Jet Airways tend to have higher average fares, certain routes such as Delhi to Cochin command premium pricing, and an increase in stops is associated with higher ticket costs. Additionally, seasonal trends and variations in flight duration further contribute to price differences.

Overall, the project highlights the importance of proper data preprocessing and feature extraction in enabling meaningful analysis, and shows how structured exploration of data can lead to practical, data-driven insights.
