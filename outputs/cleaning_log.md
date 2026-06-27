# Cleaning Log

## Project

Part 1 – Data Cleaning

## Cleaning Steps Performed

1. Created a separate `cleaned_orders.xlsx` from `raw_orders.xlsx`.
2. Preserved the original raw dataset without modification.
3. Filled 25 missing values in the `region` column with **Unknown**.
4. Filled 21 missing values in the `ship_mode` column with **Unknown**.
5. Filled 18 missing values in the `discount` column with **0**, as all related sales fields were valid.
6. Identified and flagged 15 negative discount values.
7. Removed 25 exact duplicate records.
8. Verified that there were no conflicting duplicate Order IDs.
9. Converted mixed date formats into a consistent DD/MM/YYYY format.
10. Flagged 45 records where `ship_date` occurred before `order_date`.
11. Created calculated columns:

    * calculated_sales
    * calculated_profit
    * profit_margin
    * shipping_delay_days
    * order_month
    * order_year
    * data_quality_flag
12. Verified calculated sales and profit values against the original dataset.
13. Generated the Data Quality Report.
14. Generated Pivot Summary reports.

## Assumptions

* Missing `discount` values were replaced with 0 only when all related sales fields were valid.
* Missing `region` and `ship_mode` values were replaced with **Unknown**.
* Original sales and profit columns were preserved, and separate calculated columns were created for validation and analysis.
* Negative discount values were retained in the dataset and flagged for data quality review rather than being modified.