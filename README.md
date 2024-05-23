# E-commerce-API
https://github.com/markoagidej/E-commerce-API

## Purpose
This API is designed to manage customer, their accounts, products, and orders.
A MySQL database is meant to be used along with request collection from postman.

There are 4 ways to intereact with the API:
1. Customer
2. Customer Accounts
3. Products
4. Orders

### 1. Customers
Before anything else, you must have some customers!
There are 5 requests you can make related to customers:
1.1 View all customers
1.2 View a specific customer
1.3 Add a customer
1.4 Update an existing customer
1.5 Delete a customer

#### 1.1 View all customers
endpoint: /customers
This will show all customers.
#### 1.2 View a specific customer
endpoint: /customers/<int>
Each customer is assigned a unique ID number. You will see all info related to the cusomter whose id you put at the end of the endpoint.
#### 1.3 Add a customer
endpoint: /customers
A customer can be added by placing a JSON object in the POST request with a "name", "email", and "phone".
#### 1.4 Update an existing customer
endpoint: /customers/<int>
Customer info (name, email, phone) can be updated by sending a PUT request with a JSON object containing the info at the endpoint with that customers ID.
#### 1.5 Delete a customer
endpoint: /customers/<int>
To delete a customer, send the DELETE request with the customer ID at the end.

### 2. Customer Accounts
While customers represent the actual people, a customer account is their log in info.
Each customer should only have one account!
There are 5 requests you can make related to customer accounts:
2.1 View all customer accounts
2.2 View a specific customer account
2.3 Add a customer account
2.4 Update an existing customer account
2.5 Delete a customer account

#### 2.1 View all customer accounts
endpoint: /customer_accounts
This will show all customer accounts.
#### 2.2 View a specific customer account
endpoint: /customer_accounts/<int>
Each customer account is assigned a unique ID number. You will see all info related to the account whose id you put at the end of the endpoint.
#### 2.3 Add a customer account
endpoint: /customer_accounts
A customer account can be added by placing a JSON object in the POST request with a "username", "password", and "customer_id".
The customer_id must match an existing customer entry.
#### 2.4 Update an existing customer account
endpoint: /customer_accounts/<int>
Account info (username, password) can be updated by sending a PUT request with a JSON object containing the info at the endpoint with that customers ID.
#### 2.5 Delete a customer account
endpoint: /customer_accounts/<int>
To delete a customer account, send the DELETE request with the customer account ID at the end.

### 3. Products
A Product is something to be sold to a customer via orders!
There are 5 requests you can make related to products:
3.1 View all products
3.2 View a specific product
3.3 Add a product
3.4 Update an existing product
3.5 Delete a product

#### 3.1 View all products
endpoint: /products
This will show all products.
#### 3.2 View a specific product
endpoint: /products/<int>
Each product is assigned a unique ID number. You will see all info related to the product whose id you put at the end of the endpoint.
#### 3.3 Add a product
endpoint: /products
A product can be added by placing a JSON object in the POST request with a "name", and "price".
#### 3.4 Update an existing product
endpoint: /products/<int>
Product info (name, price) can be updated by sending a PUT request with a JSON object containing the info at the endpoint with that product ID.
#### 3.5 Delete a product
endpoint: /products/<int>
To delete a product, send the DELETE request with the product ID at the end.

### 4. Orders
An order is placed by a customer and contains the customer_id.
There is an association table which keeps track of the order number and products on that order.
There are 3 requests you can make related to orders:
4.1 Place and order
4.2 View a specific order
4.3 View orders by a specific customer

#### 4.1 Place and order
endpoint: /orders
This create and order. You must provide a JSON object with a "customer_id", "date", and a list of "order_items" contained the product ids of what is to be ordered.
#### 4.2 View a specific order
endpoint: /orders/<int>
Each order is assigned a unique ID number. You will see all info related to the order whose id you put at the end of the endpoint.
#### 4.3 View orders by a specific customer
endpoint: /orders/customer/<int>
A customer might want to view all their orders. Using the customer_id at the end of this endpoint, you will see all orders this person has made.


https://github.com/markoagidej/E-commerce-API