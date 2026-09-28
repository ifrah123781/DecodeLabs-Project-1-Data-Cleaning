# DecodeLabs-Project-1-Data-Cleaning
Data Cleaning and Preparation using Python and Pandas
# Data Cleaning & Preparation

## Project Overview

This project focuses on cleaning and preparing a raw e-commerce dataset using Python and Pandas. The dataset contains 1,200 records and 14 columns related to customer orders, products, prices, payments, shipping, and order status.

The main goal was to identify and handle missing values, check duplicate records, validate dates and numerical data, clean text fields, and verify the accuracy of total prices.

## Objectives

* Identify missing or null values
* Check and remove duplicate records
* Validate date formats
* Check numerical data types and values
* Clean and validate text-based columns
* Verify calculated total prices
* Perform final data validation
* Export the cleaned dataset to Excel

## Dataset Information

* **Total Records:** 1,200
* **Total Columns:** 14
* **Tools Used:** Python, Pandas, Google Colab, Excel

### Main Columns

* OrderID
* Date
* CustomerID
* Product
* Quantity
* UnitPrice
* ShippingAddress
* PaymentMethod
* OrderStatus
* TrackingNumber
* ItemsInCart
* CouponCode
* ReferralSource
* TotalPrice

## Data Cleaning Performed

### 1. Missing Values

Missing values were identified using Pandas `isnull()`.

The `CouponCode` column contained missing values. Since a missing coupon code means that no coupon was used, the missing values were replaced with:

`No Coupon`

After cleaning, there were no remaining missing values.

### 2. Duplicate Records

Duplicate Order IDs and duplicate rows were checked.

Results:

* Duplicate Order IDs: 0
* Duplicate Rows: 0

Therefore, no duplicate records needed to be removed.

### 3. Date Validation

The `Date` column was checked and converted using Pandas `to_datetime()`.

Invalid dates were checked using `errors="coerce"`.

Results:

* Invalid Dates: 0
* Date Range: January 1, 2023 to June 30, 2025

### 4. Numerical Data Validation

The following numerical columns were checked:

* Quantity
* UnitPrice
* ItemsInCart
* TotalPrice

The numerical data types were verified and the values were checked for suspicious or incorrect entries.

### 5. Text Data Validation

Text-based columns were checked for inconsistent values and extra spaces.

The following columns were validated:

* Product
* PaymentMethod
* OrderStatus
* ReferralSource

No leading or trailing spaces were found.

### 6. Total Price Validation

The total price was independently calculated using:

`Quantity × UnitPrice`

The calculated value was compared with the original `TotalPrice`.

Results:

* Incorrect Total Prices: 0

This confirmed that the total prices in the dataset were consistent with the quantity and unit price.

## Final Validation

After completing the cleaning process:

* **Total Rows:** 1,200
* **Total Columns:** 14
* **Missing Values:** 0
* **Duplicate Rows:** 0
* **Duplicate Order IDs:** 0
* **Invalid Dates:** 0
* **Incorrect Total Prices:** 0

## How to Run

This project was developed using Google Colab.

### Option 1: Google Colab

1. Open the `.ipynb` notebook in Google Colab.
2. Upload the original Excel dataset when prompted.
3. Run the notebook cells from top to bottom.
4. The cleaned dataset will be generated as:

`Cleaned_Data_Analyst.xlsx`

### Option 2: Local Python Environment

Install the required libraries:

```bash
pip install pandas openpyxl
```

Open the notebook using Jupyter Notebook or JupyterLab and run the cells from top to bottom.

## Output

The final cleaned dataset is saved as:

`Cleaned_Data_Analyst.xlsx`

## Skills Demonstrated

* Data Cleaning
* Data Validation
* Missing Value Handling
* Duplicate Detection
* Date Formatting
* Numerical Data Validation
* Text Data Validation
* Python Basics
* Pandas
* Excel Data Preparation
* Data Quality Checking

## Project Status

**Completed — DecodeLabs Virtual Internship Project 1**
