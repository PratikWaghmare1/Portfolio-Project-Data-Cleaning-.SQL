# Layoffs 2022 Data Cleaning Project

## Overview

This project involves cleaning the 'Layoffs 2022' dataset sourced from Kaggle. The dataset contains information about layoffs across various industries, including details such as the company, location, industry, total layoffs, and more.

The primary focus of this project is to ensure data accuracy and usability by:
1. Removing duplicate records.
2. Standardizing inconsistent data.
3. Handling null values effectively.
4. Dropping unnecessary rows and columns to optimize the dataset for further analysis.

## Process

### 1. Data Duplication Handling:
- Created a staging table to work with the data safely.
- Used `ROW_NUMBER()` to identify and remove true duplicate rows based on multiple columns.

### 2. Data Standardization:
- Standardized variations in industries and country names (e.g., "Crypto Currency" to "Crypto").
- Converted inconsistent date formats to proper `DATE` type.

### 3. Null Value Management:
- Updated and filled null industry values by referencing existing records for the same company.
- Decided to keep nulls in certain numeric fields (e.g., `total_laid_off`) to allow easier analysis during the exploratory data analysis phase.

### 4. Data Cleaning:
- Removed rows with null values in key columns (`total_laid_off` and `percentage_laid_off`).
- Dropped unnecessary columns like `row_num` after processing.

## Technologies Used
- SQL (MySQL)

## Conclusion

This project highlights the importance of thorough data cleaning as a foundational step before performing any kind of data analysis or reporting.
