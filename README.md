# Diwali Sales Analysis | Power BI Dashboard

## Project Overview

This project analyses Diwali sales data to understand overall sales performance, product trends, customer patterns and shopping behaviour.

I built a two-page interactive Power BI dashboard:

- **Page 1: Diwali Sales Overview**
- **Page 2: Customer Insights**

This project was completed as part of the **DataCliq Skills Wali Diwali Data Analysis Challenge 2026**.

---

## Dataset

The dataset contains information related to:

- Orders and transaction dates
- Customers and customer segments
- Regions and states
- Products and categories
- Sales, discounts and costs
- Payment methods and sales channels
- Order status and returns
- Customer ratings
- Shipping and delivery details

---

## Tools Used

- **Power BI** – Data checking, transformation, data modelling and dashboard creation
- **Power Query** – Data transformation
- **DAX** – Creating measures and calculations

---

# Project Process

## 1. Loading the Dataset

The dataset was first loaded into Power BI.

After loading the data, I reviewed the available columns and data types to understand the structure of the dataset before starting the analysis.

---

## 2. Data Checking and Transformation in Power Query

The data was reviewed in Power Query before loading it into the Power BI model.

Reviewed the 42 columns, checked their data types and corrected the date formats in the Order Date, Ship Date and Delivery Date columns, which contained mixed formats. US and UK date formats were handled during parsing. I also inspected missing values, checked text fields for inconsistent casing, extra spaces and alternate spellings, and reviewed categorical and numeric columns for consistency. Valid blank values, such as delivery dates for orders still in transit, were retained rather than removed.

---

## 3. Creating a Star Schema

After completing the data transformation in Power Query, I organised the data into a star schema to make analysis and filtering easier.

The data model consists of one central fact table and three dimension tables:

- **Fact_Sales:** The central table containing transaction-level information, including Order ID, Order Date, Customer ID, Product ID, sales values, quantity, discounts, returns, ratings and order status.
- **Dim_Date:** A separate date table created using DAX with dates ranging from 1 January 2022 to 31 December 2025. It was used for time-based analysis, including monthly sales trends and year-over-year comparisons.
- **Dim_Customer:** Created by removing duplicate Customer IDs from the customer data. It contains customer-related attributes such as gender, age, region and customer segment.
- **Dim_Product:** Created by removing duplicate Product IDs and retaining product-related details such as product category and product tier.

### Relationships

I established one-to-many relationships between the dimension tables and the central Fact_Sales table:

- Dim_Date[Date] → Fact_Sales[Order_Date]
- Dim_Customer[Customer_ID] → Fact_Sales[Customer_ID]
- Dim_Product[Product_ID] → Fact_Sales[Product_ID]

All relationships were configured as active relationships with single-direction filtering, where the dimension tables filter the fact table.

This structure allows the dashboard to analyse sales from different perspectives, such as time, customer demographics, product categories and customer segments, while keeping the data model organised.

---

## 4. Creating Measures and Calculations

DAX measures were created to calculate the main KPIs and other metrics used in the dashboard.

Some of the key metrics include:

- Gross Sales
- Net Sales
- Units Sold
- Return Rate
- Year-over-Year Sales Growth
- Average Customer Rating

A discount range was also created to compare net sales across different discount levels.

---

# Dashboard Pages

## Page 1: Diwali Sales Overview

The first page focuses on overall sales performance.

### Key KPIs

- Gross Sales: ₹8.51 crore
- Net Sales: ₹7.61 crore
- Units Sold: 112K
- Return Rate: 8.21%
- Year-over-Year Sales Growth: 39.1%

### Visuals Used

- Monthly Sales Trend
- Sales by Region
- Daily Sales Trend Around Diwali
- Sales by Product Category
- Order Status Distribution
- Net Sales Across Discount Levels

### Slicers

- Year
- Region
- Product Tier
- Sales Channel

---

## Page 2: Customer Insights

The second page focuses on understanding the customers behind the sales.

### Key KPIs

- Total Customers: Around 8,000
- Average Rating: 4.10
- Return Rate: 8.21%

### Visuals Used

- Customer Distribution by Segment
- Sales Contribution by Gender
- Customer Distribution Across States
- Customer Ratings by Product Category
- Sales by Payment Method
- Customer Distribution by Age Group

### Slicers

- Year
- Region
- Gender
- Customer Segment

---

## Key Business Insights

- North contributed the highest share of sales, followed by West.
- Sweets and Dry Fruits were the leading product categories.
- The 1–10% discount range recorded the highest net sales.
- Returning customers formed the largest customer segment.
- Customers aged 25–44 made up a large part of the customer base.
- Customer ratings were generally positive across product categories.
