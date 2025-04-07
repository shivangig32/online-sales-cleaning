# online-sales-cleaning
This dataset contains information about online sales transactions, including transaction IDs, product categories, regions, units sold, prices, revenue, payment methods, and dates
1. Loaded the dataset

Read the CSV file into a DataFrame using pandas.


2. Handled Missing Values

Checked all columns using isnull().

No or minimal missing values were found. If any were found, you could drop or fill them.


3. Removed Duplicate Rows

Used drop_duplicates() to remove repeated entries.

This helps ensure each transaction is unique.


4. Standardized Text Values

Columns like Region, Payment Method, and Product Category were cleaned:

Removed extra spaces.

Capitalized properly (e.g., "north america" → "North America").



5. Formatted Date Values

Converted the Date column to a consistent dd-mm-yyyy format using pd.to_datetime().


6. Renamed Column Headers

Renamed all headers to:

lowercase,

no spaces (underscores used instead),

cleaned version (e.g., Unit Price → unit_price).



7. Fixed Data Types

Converted data types to appropriate types:

transaction_id → int

units_sold → int

unit_price and total_revenue → float

date → datetime



8. Validated Revenue Calculations

Recalculated revenue (units_sold * unit_price) and checked it against total_revenue.

Confirmed if there were any mismatches.


9. Saved Cleaned Dataset

Exported cleaned data to a new file:
Online_Sales_Data_Cleaned.csv
