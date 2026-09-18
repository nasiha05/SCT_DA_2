# SCT_DA_2
# Task 2 – Data Cleaning and Preparation

## Objective
Load the Global Superstore dataset into Python using Pandas, inspect it for data
quality issues, clean it, and export a cleaned CSV file ready for further analysis.

## Dataset
Global Superstore sales dataset — 51,290 rows and 27 columns, covering orders,
customers, products, sales, profit, and shipping details across multiple markets
and regions.

## Tools Used
* Python
* Pandas
* NumPy
* Google Colab

## Steps Performed

1. **Loaded the dataset** into a Pandas DataFrame and checked its shape, column
   names, and data types.
2. **Checked for missing values** — none were found in any column.
3. **Checked for duplicate rows** — none were found.
4. **Removed non-informative columns** — one column contained the same value in
   every single row and was dropped as it added no analytical value.
5. **Standardized column names and text fields** by trimming leading/trailing
   whitespace, to keep categorical values consistent.
6. **Converted Order Date and Ship Date** from text to proper datetime format.
7. **Validated the dates** — checked that no order was shipped before it was
   placed (none found).
8. **Validated the numeric fields** (Sales, Quantity, Discount) and removed 1
   row with an invalid Sales value that did not represent a real transaction.
9. **Added a few derived columns** to make the dataset easier to analyze:
   Order Year, Order Month, Shipping Days, and Profit Margin.
10. **Re-checked** the dataset for missing values and duplicates after cleaning.
11. **Exported** the final cleaned dataset to `Global_Superstore_Cleaned.csv`.

## Result

| Check | Result |
|---|---|
| Missing values | None found |
| Duplicate rows | None found |
| Non-informative columns removed | 1 |
| Invalid records removed | 1 (Sales ≤ 0) |
| Date columns converted | Order.Date, Ship.Date |
| New columns added | Order Year, Order Month, Shipping Days, Profit Margin |
| Final dataset size | 51,289 rows × 30 columns |

## Files in this Folder
* `SCT_Task2_Data_Cleaning_Preparation.ipynb` – the notebook with all cleaning steps
* `superstore.csv` – original raw dataset
* `Global_Superstore_Cleaned.csv` – final cleaned dataset
