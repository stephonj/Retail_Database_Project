# Retail_Database_Project

A MySQL database project designed to model and analyze a retail company's inventory, customer orders, and sales. This project includes an Entity-Relationship diagram, normalized schema, sample data, and analytical SQL queries.

**Features**

Normalized relational schema using MySQL

Foreign key relationships for data integrity

Sample data for customers, products, employees, suppliers, and orders

Analytical SQL queries for business insights (e.g., total sales by product, customer order history)

**Schema Overview**

The system includes the following entities:

Customers: CustomerID, FirstName, LastName, Email

Products: ProductID, Name, Category, Price, SupplierID

Suppliers: SupplierID, CompanyName, Phone

Employees: EmployeeID, FirstName, LastName, Title, Email

Orders: OrderID, CustomerID, EmployeeID, OrderDate

OrderDetails: OrderID, ProductID, Quantity, Price

**Relationships:**

A Customer can place many Orders 

An Order has many OrderDetails 

A Product can appear in many OrderDetails 

A Product belongs to one Supplier 

An Employee processes many Orders 

**Sample Queries:**

Total Sales by Product

Aggregates total revenue per product using SUM() and JOIN

Customer Order History
Lists products purchased by each customer with quantities

**Project Screenshots**
**Folder includes screenshots of:**

Table creation

Sample data inserts

Results from key SQL queries

**Technologies Used:**

MySQL
