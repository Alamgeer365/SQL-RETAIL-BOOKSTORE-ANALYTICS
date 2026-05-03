# Project Insights

This file contains the main insights I found after running the SQL queries on the sample bookstore data.

## Dataset Snapshot

- Total books: 5
- Total customers: 5
- Total orders: 8
- Total units sold: 13
- Total revenue: `$383.44`

## Key Findings

### 1. Top Revenue-Generating Books

The best-performing book is **Data Science 101**.

- `Data Science 101` sold `6` units and generated `$179.94`
- `The Art of SQL` sold `3` units and generated `$103.50`
- `Fantasy World Chronicles` generated `$45.00`
- `Learn Python the Hard Way` generated `$40.00`
- `Mystery at the Bookstore` generated `$15.00`

What this shows:
Most of the revenue is coming from just one or two books, so sales are not evenly spread across the catalog.

### 2. Inventory Risk

Only one book is below the low-stock threshold:

- `Fantasy World Chronicles` has `10` units in stock

What this shows:
This book may need restocking soon if demand continues.

### 3. Customer Value and RFM Signals

From the customer analysis:

- `Alice` is the strongest customer with `3` orders and `$104.97` in revenue
- `Charlie` generated `$89.97` from a single order
- `Bob` placed `2` orders and generated `$74.50`
- `Evan` generated `$69.00`
- `Diana` generated `$45.00`

Recency as of `2024-07-01`:

- Alice: `25` days
- Bob: `26` days
- Evan: `26` days
- Charlie: `27` days
- Diana: `27` days

What this shows:
Alice stands out as the most valuable repeat customer, while Charlie looks like a strong one-time customer with high spending.

### 4. Marketing Profitability

Profit here is calculated as `customer revenue - marketing spend`.

- Alice: `$54.97`
- Charlie: `$49.97`
- Evan: `$34.00`
- Bob: `-$0.50`
- Diana: `-$15.00`

What this shows:
Marketing spend worked well for most customers, but Bob and Diana did not generate enough revenue to cover the spend.

### 5. Sales Trend

- All recorded orders happened in `2024-06`
- Monthly revenue for `2024-06` was `$383.44`

What this shows:
There is only one month of order data, so this is not enough to study real growth or seasonality yet.

### 6. Returning Customers

Customers with more than one order:

- Alice: `3` orders
- Bob: `2` orders

What this shows:
Only two customers came back to buy again, so repeat buying is still low in this sample.

### 7. Average Order Value

- Average Order Value (AOV): `$47.93`

What this shows:
Each order brings in about `$48` on average, which is a useful number when thinking about pricing and marketing efficiency.

### 8. Cross-Purchase Patterns

The most common combinations by customer purchase history are:

- `Data Science 101` + `Mystery at the Bookstore`: `2` times
- `The Art of SQL` + `Learn Python the Hard Way`: `1` time

What this shows:
These pairings could be useful for recommendations or bundles. One thing to note is that this query shows books bought by the same customer across orders, not in the same cart.

### 9. Churn Analysis

Using the churn query with the date `2025-07-01`, all customers are marked as churned:

- Alice: `390` days since last purchase
- Bob: `391` days
- Charlie: `392` days
- Diana: `392` days
- Evan: `391` days

What this shows:
This result happens because the sample orders are from June 2024, while the churn check uses July 2025. In a real project, churn would be more useful with a larger and more recent dataset.

## Overall Takeaway

The main pattern in this dataset is that a small number of books and customers are driving most of the results. `Data Science 101` is the strongest product, Alice is the top repeat customer, and marketing looks profitable for most customers. At the same time, the dataset is small, repeat customer activity is limited, and the trend analysis is not very deep because the data only covers one month.

## Notes

- All findings are based on the sample data in `data.sql`.
- Since this is a small sample dataset, the insights are useful for practice and demonstration more than final business decision-making.
