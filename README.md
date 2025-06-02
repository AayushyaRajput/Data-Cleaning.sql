# Data-Cleaning.sql
This project involves cleaning and preparing a dataset of tech layoffs from 2022 using SQL. The data was sourced from Kaggle and cleaned by removing duplicates, standardizing formats, handling null values, and preparing it for further analysis.

Dataset Source: Kaggle - Layoffs 2022
Tools Used: MySQL (Structured Query Language)
Objective: Clean and standardize real-world layoff data from 2022 to make it suitable for analysis.

🛠️ Cleaning Steps Performed:
Staging Table Creation:

Created a copy of the original dataset (layoffs_staging) to ensure the raw data remains untouched during cleaning.

Duplicate Removal:

Used ROW_NUMBER() with a PARTITION BY clause to identify duplicate rows based on multiple key columns.

Removed true duplicates while preserving legitimate repeated entries.

Standardizing and Correcting Data:

Replaced blank industry values with NULL.

Used self-join logic to fill in missing industry fields based on company matches.

Standardized inconsistent industry names like "CryptoCurrency" → "Crypto".

Cleaned country values (e.g., removed periods from "United States.").

Converted the date column from TEXT to proper DATE format using STR_TO_DATE().

Handling Nulls:

Kept important columns like total_laid_off, percentage_laid_off, and funds_raised_millions as NULL when appropriate.

Removed rows with both total_laid_off and percentage_laid_off missing (incomplete records).

Column Cleanup:

Dropped helper column row_num after it was used to filter duplicates.

✅ Final Output:
A cleaned, structured version of the layoffs dataset in the layoffs_staging2 table.

The data is now ready for further Exploratory Data Analysis (EDA), dashboards, or machine learning models.

