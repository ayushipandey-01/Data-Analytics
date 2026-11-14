# Zepto Sales & Delivery Analysis Dashboard | Power BI

## Project Overview

The **Zepto Sales & Delivery Analysis Dashboard** is a four-page Power BI project created to explore order activity, sales performance, delivery operations, and customer purchasing patterns using a sample Zepto dataset.

The dashboard brings key metrics and charts together in an interactive report. Users can explore the data through filters such as date, city, category, store, and order status, depending on the page.

## Dataset Description

**File:** `Zepto.xlsx`

The dataset contains order-level information with the following fields:

| Column | Description |
|---|---|
| OrderID | Unique identifier for an order |
| OrderDate | Date of the order |
| City | City associated with the order |
| Store | Store associated with the order |
| CustomerID | Customer identifier |
| Category | Product category |
| OrderValue | Value of the order |
| DeliveryTime_Min | Actual delivery time in minutes |
| PromisedTime_Min | Promised delivery time in minutes |
| OrderStatus | Order status, such as Delivered or Delayed |

## Tools & Technologies

- **Microsoft Power BI** – dashboard creation, data visualization, interactive filters, and measures.
- **Microsoft Excel** – source dataset.

## Dashboard Pages

### 1. Executive Overview

This page provides a high-level view of the order and delivery data.

**KPI cards shown:**
- Total Customers
- Total Orders
- Total Order Value
- Average Order Value
- Delivered Orders
- Delayed Orders

**Visuals shown:**
- Total Order Value by Date
- Total Orders by City
- Average Delivery and Promised Time by City
- Total Order Value by Category
- Order Status Distribution
- Average Delivery Time by City

The page helps users review order volume, order value, category contribution, city-level activity, and the split between delivered and delayed orders.

![Executive Overview dashboard](screenshots/01-executive-overview.png)

### 2. Sales & Category Analysis

This page focuses on order value and category performance, with additional comparisons across cities and stores.

**KPI cards shown:**
- Total Category
- Total Orders
- Total Order Value
- Average Order Value
- Top Performing Category

**Visuals shown:**
- Total Order Value by Category
- Category Distribution to Total Order Value
- Total Orders and Total Order Value by Category
- Total Order Value by City
- Total Order Value by Store
- Total Customers by Store and Category

The page supports comparisons of category contribution and order value across the available city and store fields. The screenshot shows the City filter set to Pune, so the displayed KPI values and charts on this page reflect that selection rather than an unfiltered dataset total.

![Sales and Category Analysis dashboard](screenshots/02-sales-category-analysis.png)

### 3. Delivery Performance

This page examines delivery status and compares actual delivery time with promised delivery time.

**KPI cards shown:**
- Total Orders
- Delivered Orders
- Delayed Orders
- Deliver Rate %
- Average Delivery Time
- Average Promised Time

**Visuals shown:**
- Delivered vs Delayed Orders
- Average Delivery Time by City
- Actual vs Promised Time by City
- Delayed Orders by City
- Delivery Time by Store
- Order Status by Store

These visuals make it possible to compare delivery timing across cities and stores and to view the distribution of delivered and delayed orders.

![Delivery Performance dashboard](screenshots/03-delivery-performance.png)

### 4. Customer & Order Analysis

This page explores customer counts, order frequency, order value, and how orders are distributed across cities, stores, and categories.

**KPI cards shown:**
- Total Customers
- Total Orders
- Average Customer per Order
- One-Time Customer
- Average Order Value

**Visuals shown:**
- Total Orders by CustomerID
- Total Customers by Store
- Total Customers and Order Value by Category
- Customer-wise Order Value
- Customer Distribution by City
- Order Status by Category

The page provides a view of customer and order patterns within the available sample. In the displayed report, the one-time customer KPI is 40; this is a result shown by the current report, not a claim about Zepto's overall customer base.

![Customer and Order Analysis dashboard](screenshots/04-customer-order-analysis.png)

## Interactive Dashboard Features

- Page navigation between the four dashboard sections.
- KPI cards for key order, sales, delivery, and customer measures.
- Slicers to filter the report by available dimensions, including date, city, category, store, and order status.
- Charts that support comparisons across categories, cities, stores, and order statuses.

## Project Objective

The objective of this project is to present order-level data in a clear, interactive dashboard and practise analysing sales, delivery, and customer-related metrics using Power BI.

## Dataset Limitation

This project is based on the supplied sample dataset. The results represent only the records included in that dataset and should not be interpreted as Zepto's actual company-wide business performance.

## Author

**Ayushi Pandey**

**Project:** Zepto Sales & Delivery Analysis Dashboard  
**Tool:** Microsoft Power BI
