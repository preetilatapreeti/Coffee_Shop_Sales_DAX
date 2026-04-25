# Data Dictionary

This document describes the columns in `data/Coffee Shop Sales.csv`. The dataset contains point-of-sale transaction records for a coffee shop chain across multiple store locations.

## Columns

- `transaction_id` (integer)
  - Unique identifier for each transaction record.
  - Example: `1`

- `transaction_date` (date string)
  - The date when the transaction occurred.
  - Format: `M/D/YY`.
  - Example: `1/1/23`

- `transaction_time` (time string)
  - The time of day when the transaction was recorded.
  - Format: `H:MM:SS` using 12-hour clock without AM/PM.
  - Example: `7:06:11`

- `transaction_qty` (integer)
  - Number of items sold in the transaction line.
  - Example: `2`

- `store_id` (integer)
  - Numeric identifier for the store location where the sale occurred.
  - Example: `5`

- `store_location` (string)
  - Human-readable name of the store location.
  - Example: `Lower Manhattan`

- `product_id` (integer)
  - Numeric identifier for the sold product.
  - Example: `32`

- `unit_price` (decimal)
  - Price per unit of the product sold.
  - Example: `3` or `3.10`

- `product_category` (string)
  - Broad category of the product sold.
  - Examples: `Coffee`, `Tea`, `Drinking Chocolate`

- `product_type` (string)
  - Product subcategory or style.
  - Example: `Gourmet brewed coffee`

- `product_detail` (string)
  - Additional product description, typically including flavor or size details.
  - Example: `Ethiopia Rg`

## Notes

- `transaction_date` and `transaction_time` are separate fields, so combining them into a single timestamp may simplify time-series analysis.
- `transaction_qty` is the quantity at the line-item level; aggregated revenue should use `transaction_qty * unit_price`.
- Use `store_id` and `store_location` together to verify location mapping.
- `product_category`, `product_type`, and `product_detail` can be used for tiered product grouping and inventory analysis.
