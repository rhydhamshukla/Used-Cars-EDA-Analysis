# Exploratory Data Analysis on Used Cars Dataset

**Student:** Rhydham Shukla  
**Course:** Machine Learning Program, Unlox Academy  
**Project:** Minor Project 1 (Exploratory Data Analysis)  

## Project Overview
This project delivers a comprehensive Exploratory Data Analysis (EDA) on the genuine Kaggle CarDekho Used Car Details v3 dataset (8,128 raw listings).

The objective is to analyze key drivers of used car valuation, quantify mileage depreciation, examine brand residual values, and evaluate fuel and transmission premiums while maintaining rigorous data quality through duplicate removal and Interquartile Range (IQR) outlier filtering.

## Data Quality and Preprocessing Pipeline
1. **Raw Dataset:** 8,128 listings across 13 automotive attributes.
2. **Duplicate Removal:** Identified and eliminated 1,202 duplicate listings, preserving 6,926 unique vehicles.
3. **Feature Parsing:** Converted text fields (`mileage`, `engine`, `max_power`) into numerical measurements (kmpl, CC, bhp). Extracted manufacturer brand from vehicle names.
4. **IQR Outlier Filtering:**
   * Selling Price Upper Fence: Rs 1,208,750 (Rs 12.08 Lakhs), removing 328 extreme luxury outliers.
   * Kilometers Driven Upper Fence: 190,000 km, removing 167 commercial extreme mileage outliers.
   * Clean Analytics Sample: 6,431 records retained (92.9% of unique data).

## Visual Analysis (6 Charts across 5 Chart Types)
* **Chart 1 (Histogram & KDE):** Compares raw vs cleaned price distributions, showing normal consumer density centered between Rs 2.5L and Rs 6.5L.
* **Chart 2 (Boxplot):** Compares price spreads across top 6 brands, highlighting Toyota (Rs 7.1L median) and Mahindra (Rs 6.5L median) for strong residual value.
* **Chart 3 (Scatter Plot):** Illustrates price decay vs kilometers driven, revealing a persistent price markup for automatic transmissions.
* **Chart 4 (Bar Chart):** Compares fuel types, showing Diesel cars average Rs 5.51 Lakhs compared to Petrol at Rs 3.99 Lakhs, with CNG and LPG trading at discounts.
* **Chart 5 (Countplot):** Examines ownership tiers, showing First Owners represent over 65% of listings while Third or higher owners drop below 8%.
* **Chart 6 (Heatmap):** Measures correlation across specifications, finding Horsepower (r = 0.68) and Engine CC (r = 0.53) are the strongest valuation drivers.

## Repository Structure
* `Used_Cars_EDA_Analysis.ipynb`: Fully executed Jupyter notebook with all code, outputs, and embedded figures.
* `Rhydham_Shukla_Minor_Project_1_Report.pdf`: One page summary report.
* `car_details_v3.csv`: Genuine Kaggle CarDekho dataset.
* `car_details_cleaned.csv`: Cleaned dataset after duplicate and IQR filtering.
* `requirements.txt`: Python package requirements.

## How to Run
1. Clone this repository:
   git clone https://github.com/rhydhamshukla/Used-Cars-EDA-Analysis.git
2. Install dependencies:
   pip install -r requirements.txt
3. Open the notebook:
   jupyter notebook Used_Cars_EDA_Analysis.ipynb
