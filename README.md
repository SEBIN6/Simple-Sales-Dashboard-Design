# Power BI Sales Dashboard: Superstore Dataset

This repository contains a Power BI dashboard built using a cleaned version of the Superstore dataset (`Cleaned_train.csv`). The dashboard provides insights into sales trends over time, performance by region, and category-level sales analysis.

## 📁 Files Included

- `Superstore_Dashboard.pbix` – Power BI dashboard file.
- `Cleaned_train.csv` – Cleaned dataset used for visualization.

---

## 📊 Dashboard Overview

### 1. **Line Chart: Sales Trend by Month-Year**
- **X-Axis:** `Month-Year` (custom field)
- **Values:** `Sales` (aggregated as **Sum**)
- **Sorted by:** `Order Date`
- **Insight:** Peaks observed in November 2017, indicating seasonal trends (e.g., holiday season).

### 2. **Bar Chart: Sales by Region**
- **Axis:** `Region` (Central, East, South, West)
- **Values:** `Sales` (Sum)
- **Sorted by:** Sales (Descending)
- **Insight:** The **West** region leads in sales, contributing ~35% of the total.

### 3. **Donut Chart: Sales by Category**
- **Legend:** `Category` (Furniture, Office Supplies, Technology)
- **Values:** `Sales` (Sum)
- **Insight:** **Technology** products dominate the sales share (~40%).

### 4. **Slicer: Region Filter**
- Enables filtering the entire dashboard by selected region.
- Format: Dropdown for clean UI.
  
---

## 🛠️ Data Preparation Steps

1. **Import Data into Power BI**:
   - Go to **Home > Get Data > Text/CSV**
   - Load `Cleaned_train.csv`.

2. **Ensure Column Types**:
   - `Order Date`: Date
   - `Sales`: Decimal Number
   - `Region` & `Category`: Text

3. **Create `Month-Year` Field** in Power Query:
   - Add `Month` and `Year` columns.
   - Create a custom column:  
     ```powerquery
     MonthYear = [Month] & "-" & Text.From([Year])
     ```
   - Sort `MonthYear` using a helper column (`Order Date` or `YearMonth`).

---

## 💡 Key Insights

1. **The West region** had the highest sales, contributing ~35% of the total.
2. **Technology** was the top-selling category (~40% share).
3. **Sales peaked in November 2017**, likely due to holiday demand.
4. **The Central region** had the lowest sales, indicating potential growth opportunities.

---

## 📌 Dataset Summary

- Rows: ~9800
- Years Covered: 2015–2018
- Regions: Central, East, South, West
- Categories: Furniture, Office Supplies, Technology

---

## 📈 Tools Used

- **Power BI Desktop**
- **Microsoft Power Query Editor**
- **Python (Google Colab)** – for initial cleaning of raw data

---
