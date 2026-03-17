 # Superstore Sales Data Cleaning Project

 ## Project Overview
This project focuses on cleaning and preparing a raw **Superstore sales dataset** using **Microsoft Excel** so that it can be used for data analysis.

Raw datasets often contain missing values, inconsistent formatting, and other data quality issues. The goal of this project is to clean the dataset and transform it into a structured format suitable for business analysis.

This project demonstrates fundamental data preparation skills used in real-world analytics workflows.

## Tools Used
- Microsoft Excel – Data cleaning and transformation
 - GitHub – Project documentation
 
  ## Dataset Information

 ## Source : Kaggle
  
The dataset contains **9,800 rows and 18 columns** representing sales transactions of a retail superstore.

### Key Fields
- Order ID
- Order Date
- Ship Date
- Customer Name
- Segment
- City
- State
- Postal Code
- Region
- Product ID
- Category
- Sub-Category
- Product Name
- Sales

- ---

## Data Cleaning Tasks Performed

### 1. Removed Duplicate Records
Duplicate rows can distort analysis results.

**Method**
- Used Excel's **Remove Duplicates** feature.
- Checked duplicates based on:
  - Order ID
  - Product ID

This ensured each order-product pair appears only once.

---

### 2. Handled Missing Values
The dataset contained **11 missing values** in the **Postal Code** column.

**Solution**
- Used **Go To Special → Blanks** in Excel.
- Replaced blank values with:

```
Unknown
```

---

### 3. Standardized Text Formatting
Some text fields contained extra spaces or inconsistent formatting.

**Columns Cleaned**
- Customer Name
- City
- State
- Product Name

**Functions Used**

```
TRIM()
PROPER()
```

These functions remove extra spaces and standardize capitalization.

---

### 4. Verified Data Types
Ensured the following columns were properly formatted:

| Column | Format |
|------|------|
| Order Date | Date |
| Ship Date | Date |
| Sales | Currency/Number |

Correct data types are necessary for accurate calculations and visualization.

---

### 5. Created Shipping Days Column
A new column was created to measure delivery performance.

**Formula**

```
=Ship Date - Order Date
```

This calculates the number of days taken to ship an order.

---

### 6. Created Analytical Time Columns
Additional time-based fields were created to support analysis in Tableau.

| Column | Formula |
|------|------|
| Year | `=YEAR(OrderDate)` |
| Month | `=TEXT(OrderDate,"MMMM")` |
| Quarter | `="Q"&ROUNDUP(MONTH(OrderDate)/3,0)` |

These columns help analyze sales trends over time.

---

## Final Cleaned Dataset
After cleaning, the dataset includes additional analytical columns such as:

- Shipping Days
- Year
- Month
- Quarter


