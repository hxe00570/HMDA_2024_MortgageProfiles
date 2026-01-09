# HMDA Loan Characteristics by Race & Gender
This repository contains exploratory analysis of the Home Mortgage Disclosure Act (HMDA) loan application data for 2024. The analysis focuses on visualizing rate_spread, debt_to_income_ratio, loan_amount, and loan_to_value_ratio broken down by derived_race and derived_sex.

## Overview
This notebook processes over 12.2 million loan applicant records from the 2024 HMDA dataset. It specifically filters for single applicants who applied for a primary mortgage on a single-family home (1-4 units) and whose data is complete for the key attributes under investigation. The analysis includes data cleaning to remove outliers and visualize the relationships between loan characteristics and demographic factors.

## Setup
To run this notebook, a High-Ram Python GPU instance is recommended, as some computational steps (e.g., KDE plots) can be time-intensive (10-20 minutes).

## Installation
Ensure you have Python installed. Then, install the necessary dependencies using pip:

pip install pandas numpy seaborn matplotlib statsmodels

Google Drive Setup
The notebook expects the HMDA 2024 data file (year_2024.csv) to be mounted from Google Drive. Ensure your Google Drive is mounted to /content/drive and the file is located at '/content/drive/MyDrive/CIS-2330_Database_Fundamentals/year_2024.csv' (or adjust the path in the notebook accordingly).

## Data
The dataset used is the 2024 Home Mortgage Disclosure Act (HMDA) loan application data. 

The primary file is year_2024.csv. 

### Key columns analyzed include:
derived_sex
derived_ethnicity
derived_race
loan_to_value_ratio
debt_to_income_ratio
rate_spread
interest_rate
loan_amount
occupancy_type
loan_type
loan_purpose
action_taken (used to determine loan approval)

Data cleaning involves removing 'sex not available', 'joint', 'ethnicity not available', 'free form text only', and 'race not available' categories. Outliers in numerical variables (debt_to_income_ratio, rate_spread, loan_amount, loan_to_value_ratio) are filtered using 1st and 99th percentiles.

## Analysis Highlights
Loan Approval Rates: Comparison of loan approval rates across different racial and gender groups.
Rate Spread Distributions: Visualization of rate spread distributions by race and gender, including KDE plots to understand joint distributions.

Loan Characteristics: Analysis of mean loan amounts, debt-to-income ratios, and loan-to-value ratios across demographic groups.

2D KDE Plots: In-depth visualizations showing the joint distributions of:
rate_spread vs. debt_to_income_ratio
loan_to_value_ratio vs. debt_to_income_ratio
loan_amount vs. loan_to_value_ratio


