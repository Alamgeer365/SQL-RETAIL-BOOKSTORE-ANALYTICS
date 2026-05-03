# SQL Retail Bookstore Analytics

This is a small SQL project where I analyzed bookstore sales data. I created a simple database with books, customers, orders, and marketing spend, then wrote queries to answer common business questions around sales, inventory, and customer behavior.

## About the Project

The main goal was to practice SQL in a way that feels closer to a real business use case. Instead of only writing basic queries, I wanted to look at the kind of questions a bookstore team might actually ask, such as:

- Which books generate the most revenue?
- Which books are running low on stock?
- Which customers are most valuable?
- Is marketing spend leading to profit?
- Are customers coming back to buy again?

## Database Structure

The database has four tables:

1. `Books`
   Contains book details like title, genre, price, and stock.

2. `Customers`
   Stores customer information such as name, city, and signup date.

3. `Orders`
   Records which customer bought which book, along with quantity and order date.

4. `MarketingSpend`
   Stores the marketing amount spent for each customer.

These tables are connected using primary and foreign keys so the sales and customer data can be analyzed together.

## Files Included

- `schema.sql` - table creation script
- `data.sql` - sample data for the project
- `analysis_queries.sql` - business analysis queries
- `README.md` - project overview

## What I Analyzed

In this project, I wrote queries for:

- revenue by book
- low-stock books
- customer RFM-style analysis
- marketing profit by customer
- monthly sales trend
- returning customers
- average order value
- books often bought by the same customer
- churned customers

## SQL Skills Used

This project helped me practice:

- table creation and schema design
- joins across multiple tables
- aggregate functions like `SUM()`, `COUNT()`, and `ROUND()`
- `GROUP BY`, `ORDER BY`, and `HAVING`
- CTEs using `WITH`
- date functions like `STRFTIME()` and `julianday()`
- writing queries around business metrics

## How to Run the Project

This project is written in a SQLite-friendly style because it uses functions like `STRFTIME()` and `julianday()`.

1. Create a new SQLite database.
2. Run `schema.sql` to create the tables.
3. Run `data.sql` to insert sample data.
4. Run `analysis_queries.sql` to view the analysis.

## What I Learned

This project helped me understand how SQL can be used for more than just fetching rows. I got better at joining tables, building business-focused queries, and turning raw data into simple insights. I also practiced thinking from a business point of view, not just a technical one.

Some of the main things I learned were:

- how to design a simple relational database
- how to connect multiple tables for analysis
- how to calculate metrics like revenue, AOV, and customer value
- how to use CTEs and date functions in real queries
- how SQL supports decisions in sales, inventory, and marketing

## Final Note

This project is small, but it gave me a good foundation in SQL analytics and helped me build something that feels practical enough for a portfolio.
