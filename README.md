# Task-1--Data-Cleaning-and-Preprocessing

# Sales Dataset Cleaning and Preprocessing

## Overview

This repository contains a notebook that demonstrates the process of cleaning and preprocessing a sales dataset. The purpose is to prepare the data for further analysis, ensuring it's in a clean, consistent, and usable format.

## Project Steps

The following steps were performed in the notebook:

### 1. Import Required Libraries
The necessary libraries, such as `pandas`, were imported for data manipulation and processing.

### 2. Load Dataset
The sales dataset (`sales_data_sample.csv`) was loaded into a pandas DataFrame for processing.

### 3. Drop Unnecessary Columns
Unnecessary columns such as `PHONE`, `ADDRESSLINE2`, `POSTALCODE`, `CONTACTLASTNAME`, and `CONTACTFIRSTNAME` were dropped to simplify the dataset.

### 4. Handle Missing Values
- Missing values in the `STATE` column were filled with the most frequent value (mode).
- Rows with missing `CUSTOMERNAME` were dropped since this is a crucial field.

### 5. Remove Duplicate Rows
Any completely duplicated rows were removed to ensure uniqueness in the dataset.

### 6. Standardize Text Values
All object-type (string) columns were converted to lowercase for consistency, ensuring that similar values with different cases are treated as the same.

### 7. Convert Date Columns
The `ORDERDATE` column was converted to a proper datetime object using `pd.to_datetime()`, enabling easier manipulation of date-related data.

### 8. Rename Columns Uniformly
Column names were standardized by converting them to lowercase and replacing spaces with underscores, ensuring uniformity and easier use.

### 9. Check & Fix Data Types
Numeric columns such as `quantityordered` and `priceeach` were converted to the appropriate numeric types to ensure correct calculations.

### 10. Outlier Treatment (Optional)
Using the Interquartile Range (IQR) method, outliers in the `quantityordered` column were removed to maintain the integrity of the dataset.

### 11. Save the Cleaned Dataset
After cleaning, the dataset was saved as `cleaned_sales_data.csv` for further analysis.

## Key Learnings

- **Data Cleaning** is essential for meaningful analysis and ensures reliable results.
- **Data Standardization** (like converting text to lowercase) reduces inconsistencies.
- **Outlier Handling** prevents skewed results from extreme values.
- **Datetime Conversion** makes date-based analysis easier.
- Saving the cleaned dataset allows for reproducibility and further analysis.

## Files in this Repository

- **sales_data_sample.csv**: Original dataset.
- **cleaned_sales_data.csv**: Cleaned and preprocessed dataset.
- **sales_data_cleaning_notebook.ipynb**: Jupyter notebook that contains the entire cleaning and preprocessing process.


