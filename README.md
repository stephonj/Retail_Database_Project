# Retail_Database_Project

A MySQL database project designed to model and analyze a retail company's inventory, customer orders, and sales. This project includes an Entity-Relationship diagram, normalized schema, sample data, and analytical SQL queries.

# Business Questions Answered
How much revenue has each product generated?

What has each customer purchased, and in what quantities?

For each order, who bought it, which employee handled it, and what was the total?

Which customers have never placed an order?

Which orders were larger than the average order?

How do products rank by revenue?
# Features
Normalized relational schema with primary and foreign keys for data integrity

Sample data for customers, products, suppliers, employees, and orders

Six analytical queries covering aggregation, joins, a CTE, and a window function

Full lifecycle: schema design, data population, query execution, reporting
# Schema Overview
**Table	& Columns**
Customers	CustomerID, FirstName, LastName, Email

Products	ProductID, Name, Category, Price, SupplierID

Suppliers	SupplierID, CompanyName, Phone

Employees	EmployeeID, FirstName, LastName, Title, Email

Orders	OrderID, CustomerID, EmployeeID, OrderDate

OrderDetails	OrderID, ProductID, Quantity, Price

# Relationships

A customer can place many orders.

An order has many order details.

A product can appear in many order details.

A product belongs to one supplier.

An employee processes many orders.
# Files
schema.sql	Creates the RetailSystem database and all six tables

sample_data.sql	Inserts sample customers, suppliers, products, employees, orders, and order details

queries.sql	Six analytical queries, each commented with the question it answers

screenshots/	Screenshots of table creation, data inserts, and query results

Retail_Database_Project_Write-Up.pdf	Project write-up
# How to Run

Requires MySQL 8.0 or later (the CTE and window-function queries need it).

Run the scripts in this order from the MySQL command line, from the folder containing the files:
bash
   mysql -u root -p < schema.sql
   mysql -u root -p < sample_data.sql
   mysql -u root -p < queries.sql

# Queries
Total sales by product: revenue per product (SUM with GROUP BY)

Customer order history: products purchased by each customer, with quantities (multi-table join)

Order summary: customer, employee, and total for each order (four-table join)

Customers with no orders: LEFT JOIN with an IS NULL filter

Orders above the average order total: CTE with a subquery

Product revenue ranking: window function (RANK)
