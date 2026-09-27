# SWYNEX - Final Data Analytics Project

## Problem Statement :
Analyze raw e-commerce sales data to identify revenue trends, top-performing categories and cities, customer payment preferences, and overall business performance — and present the findings through an interactive dashboard to support data-driven decision-making.

## Dataset Information:
- **Source file:** `raw_sales_dataset.csv`
- **Original size:** 2160 rows × 9 columns
- **Final cleaned size:** 2000 rows × 9 columns (+ derived Revenue column)
- **Columns:** OrderID, CustomerName, City, Category, Quantity, Price, OrderDate, PaymentMode, Rating

## Data Cleaning Process:
- Removed **124 duplicate records**
- Standardized **City** names — merged 73 inconsistent variations (e.g. `MUMBAI`, `mumbai `, `Mumbai`) into 15 clean city names
- Fixed **Rating** column — converted text values like `"five"` into numeric `5`
- Converted **OrderDate** to a proper date format (handled multiple mixed date formats)
- Filled missing **Quantity**, **Price**, and **Rating** values using the median
- Filled missing **PaymentMode** using the mode (most frequent value)
- Filled missing **CustomerName** with `"Unknown"` (62 records)
- Re-checked and confirmed **zero duplicates and zero missing values** after cleaning
- Exported the final cleaned dataset as `cleaned_sales_dataset.csv`

##  Exploratory Data Analysis:
- Created a derived **Revenue** column (`Quantity × Price`)
- Calculated summary statistics:
  - **Total Revenue:** ₹73.37M
  - **Average Order Value:** ₹36,685
  - **Average Rating:** 3.53
- Performed the following analyses:
  1. Revenue by Category
  2. Monthly Revenue Trend
  3. Revenue by City (Top 10)
  4. Payment Mode Usage
  5. Rating Distribution
  6. Correlation Heatmap (Quantity, Price, Rating, Revenue)

## 📈 Dashboard
An interactive Sales Performance Dashboard was built using **Power BI**, featuring KPIs, category and city-wise revenue charts, a monthly revenue trend line, payment mode distribution, and dynamic City/Category filters.

## 💡 Key Business Insights:
- **Stationery** is the top-performing category, generating the highest revenue (10.3M)
- **Pune** and **Bangalore** are the top revenue-generating cities
- **Cash on Delivery** is the most preferred payment mode, used in 28% of transactions
- Average customer rating stands at **3.53 out of 5**, indicating moderate customer satisfaction
- Revenue shows noticeable month-to-month fluctuation, suggesting seasonal buying patterns

## 🛠️ Tools Used:
- Python (Pandas, NumPy) — Data Cleaning & EDA
- Matplotlib, Seaborn — Visualization
- Power BI — Interactive Dashboard

##  Files in this Repository:
- `01-task.ipynb` – Data Cleaning & Preparation notebook
- `02-task.ipynb` – Exploratory Data Analysis notebook
- `SWYNEX-Sales-Dashboard.pbix` – Power BI dashboard file
- `raw_sales_dataset.csv` – Original raw dataset before cleaning
- `cleaned_sales_dataset.csv` – Final cleaned dataset used for analysis

## 🙌 Acknowledgment
This project was completed as part of my Data Analytics Internship with **SWYNEX Technologies**, combining Tasks 1, 2, and 3 into one complete case study.

#SWYNEX #Internship #DataAnalytics #PowerBI #Python
