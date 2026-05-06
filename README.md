# Osta-Limited-Sales-Analysis-Dashboard-Tableau-
## Project Overview
This project analyzes retail sales data for Osta Limited, a company involved in the sale of goods across multiple regions and product categories. The goal is to deliver interactive dashboards that provide insights into sales performance, profitability, customer behavior, and regional trends.

The dashboards were built using Tableau and focus on year-over-year comparisons, KPIs, and drill-down analysis.

## 📁 Dataset Description
The project uses four main tables:
1. Customers Table
    * Customer ID
    * Customer Name
2. Location Table
    *   Postal Code
    *   City
    *   State
    *   Region (East, West, South, Central)
    *   Country
3. Orders Table
    *   Row ID
    *   Order ID
    *   Order Date
    *   Ship Date
    *   Ship Mode
    *   Customer ID
    *   Segment
    *   Postal Code
    *   Product ID
    *   Sales
    *   Quantity
    *   Discount
    *   Profit
4. Products Table
    *   Product ID
    *   Category (Furniture, Office Supplies, Technology)
    *   Sub-Category
    *   Product Name

## ⚙️ Data Preparation
  * Imported CSV files into Tableau
* Established relationships between tables:
     * Customers ↔ Orders
     * Orders ↔ Products
     * Orders ↔ Location
* Verified and corrected data types
* Created calculated fields for time-based analysis

## 📅 Key Features & Calculations
🔹 Year Parameter

Created a dynamic parameter Select Year to allow users to switch between reporting periods and enable year-over-year analysis.

🔹 Year Extraction

A calculated field was created to extract the year from the order date, making it easier to use in filters and parameter-driven calculations.

`IF [PY Sales] != 0 THEN ([CY Sales] - [PY Sales]) / [PY Sales] END`




















