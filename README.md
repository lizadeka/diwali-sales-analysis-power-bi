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

The process included checking:

- Column names
- Data types
- Missing or blank values
- Date-related columns
- Sales and other numeric fields
- Data consistency

The required transformations were then made to prepare the data for analysis.

---

## 3. Creating a Star Schema

After checking and transforming the data, I created a star schema for the Power BI model.

The model separates the main sales data from the supporting dimension tables.

The main tables include:

- **Fact Sales** – Contains the main sales and order-related information.
- **Date Table** – Used for date and time-based analysis.
- **Customer Table** – Contains customer-related information.
- **Product Table** – Contains product and category details.

Relationships were created between the fact table and dimension tables to support filtering and analysis across the dashboard.

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

---

## Dashboard

The dashboard allows users to interact with the data using slicers and explore sales and customer patterns from different perspectives.
