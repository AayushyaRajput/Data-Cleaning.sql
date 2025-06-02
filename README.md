📊 Data Cleaning with SQL — Tech Layoffs 2024
This project focuses on cleaning and preparing a real-world dataset of tech layoffs from 2024 using SQL. The goal is to make the data consistent, reliable, and ready for further analysis such as EDA, dashboards, or machine learning applications.

📁 Dataset Source
Kaggle: Layoffs 2024 (Provide exact link if available)

🛠️ Tools Used
MySQL — Structured Query Language for data manipulation and cleaning

🎯 Objective
To clean and standardize raw layoff data to ensure it’s analysis-ready — addressing duplicates, inconsistent formats, missing values, and more.

🧼 Cleaning Workflow
🗂️ 1. Staging Table Creation
Created a staging table layoffs_staging to preserve the raw dataset.

Ensured original data remains untouched during transformations.

🧮 2. Duplicate Removal
Applied ROW_NUMBER() with PARTITION BY to detect duplicates across key columns (company, location, etc.).

Removed exact duplicates while keeping valid repeated entries.

🛠️ 3. Data Standardization
Replaced empty industry values with NULL.

Populated missing industry data using a self-join based on matching company names.

Standardized inconsistent labels like:

"CryptoCurrency" → "Crypto"

Cleaned country names:

"United States." → "United States"

Converted string date fields into SQL DATE format using STR_TO_DATE().

❓ 4. Null Handling
Retained NULL in fields like total_laid_off, percentage_laid_off, and funds_raised_millions where data was missing but valid.

Removed rows where both total_laid_off and percentage_laid_off were missing — these were incomplete records.

🧹 5. Column Cleanup
Dropped the temporary row_num column used during duplicate filtering.

✅ Final Output
A clean, structured, and reliable version of the layoff dataset stored in the layoffs_staging2 table.

🧪 Ready for:

Exploratory Data Analysis (EDA)

Dashboard visualizations

Machine Learning workflows

📌 Summary
✅ Cleaned & deduplicated

✅ Standardized formats

✅ Null values handled

✅ Analysis-ready dataset

