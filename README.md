# 🧹 Cafe Sales Data Cleaning Project

## 📌 Project Overview

This project focuses on cleaning and standardizing a real-world cafe sales dataset containing missing values, invalid entries, and inconsistent data types. The goal is to prepare a reliable, analysis-ready dataset suitable for downstream analytics and visualization.

--- 

## 🗂 Dataset Description

The dataset includes transaction-level cafe sales data with the following key fields:

- transaction_id

- item

- quantity

- price_per_unit

- total_spent

- payment_method

- location

- transaction_date

The raw data contains common real-world issues such as:

- Missing values

- Invalid string entries in numeric fields

- Inconsistent text formatting

- Invalid date values

---

## 🔧 Data Cleaning Steps

### 1. Initial Inspection

- Reviewed data structure, types, and missing values

- Standardized column names using snake_case

### 2. Date Handling

- Converted transaction_date to datetime format

- Invalid date values were safely handled using coercion

### 3. Numeric Column Cleaning

- Converted quantity, price_per_unit, and total_spent to numeric types

- Invalid string values were coerced to null

- Negative and zero values were identified and removed where necessary

### 4. Categorical Data Standardization

- Standardized string columns by trimming whitespace

- Replaced invalid values such as "error" with "Unknown"

- Missing categorical values were retained and labeled as "Unknown" to preserve data volume

### 5. Logical Imputation

Imputed missing values when possible using known relationships:

- quantity = total_spent / price_per_unit

- price_per_unit = total_spent / quantity

- total_spent = quantity × price_per_unit

### 6. Row Removal (Minimal & Justified)

Rows with missing numerical values that could not be logically imputed were removed, as they would invalidate revenue calculations

---

## 📊 Final Output

Cleaned, standardized dataset ready for:

- Exploratory data analysis

- SQL querying

- Power BI / Tableau dashboards

- Data quality issues are explicitly documented rather than hidden

---

## 🛠 Tools & Technologies

- Python

- Pandas

- NumPy

- Jupyter Notebook

---

## 🎯 Key Takeaways

- Demonstrates real-world data cleaning practices

- Focuses on business logic, not just technical fixes

- Emphasizes transparency and data quality awareness

---

## 🚀 Next Steps

- Perform exploratory data analysis (EDA)

- Build a sales or revenue dashboard

- Use cleaned data for SQL or Power BI projects
