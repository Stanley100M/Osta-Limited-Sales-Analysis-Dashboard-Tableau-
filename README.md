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
**🔹 Year Parameter**

Created a dynamic parameter Select Year to allow users to switch between reporting periods and enable year-over-year analysis.

**🔹 Year Extraction**

A calculated field was created to extract the year from the order date, making it easier to use in filters and parameter-driven calculations.

`YEAR([Order Date])`

**🔹 Current Year Sales (CY Sales)**

Calculates total sales for the selected year.

`SUM(
    IF YEAR([Order Date]) = [Select Year] THEN [Total Sales]
    END
)`

**🔹 Previous Year Sales (PY Sales)**

Calculates total sales for the year preceding the selected year.

`SUM(
    IF YEAR([Order Date]) = [Select Year] - 1 THEN [Total Sales]
    END
)`

**🔹 Year-over-Year % Difference**

Measures the percentage change in sales between the current and previous year.

`IF [PY Sales] != 0 THEN
    ([CY Sales] - [PY Sales]) / [PY Sales]
END`

**🔹 Key Insight**

These calculations enable dynamic year-over-year comparison, helping identify sales growth trends and performance gaps across different time periods.

## 📈 Dashboard Development
**1. Sales Performance Dashboard**

This displays key sales indicators

![Sales Dashboard](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Sales%20Dashboard.png)

**2. 📈 Month-over-Month Trend Analysis**

Overall change in **sales**

![Month on Month Sales](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Month%20on%20Month%20sales.png)

Overall change in **Discount**

![Month on Month Discount](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Month%20on%20Month%20Discount.png)

Overall change in **Profit**

![Month on Month Profit](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Month%20on%20Month%20Profits.png)

**3. 📊 Category & Sub-Category Performance**

Perfomance by sub-category

![Sub Category Sales Perfomance](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Sub-category%20Salees%20and%20Profit%20view.png)

**4. 📅 Weekly Trends against Average Line**

Weekly average **sales and profit**

![Weekly sales and profit](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Weekly%20Profit%20and%20Sales%20Trend.png)

**5. 👥 Customer Dashboard**

Number of **orders per customer**

![Orders per Customer](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Orders%20per%20Customer.png)

**Top 10** customers by profit

**Rank** of customers by profit

![Top 10 customers by profit](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Top%2010%20Customers%20by%20Profit.png)

**Cross-filtering** across all visuals on Customer Dashboard

Dynamic **filters** for easy navigation

![Filters](https://github.com/Stanley100M/Osta-Limited-Sales-Analysis-Dashboard-Tableau-/blob/main/images/Customer%20Dashboard.png)

## 📊 Key Insights

**1. Revenue ≠ Profit**

Some high-revenue products **(e.g., Tables, Supplies, ookcases)** generated low or negative profit, largely due to heavy discounting.

**Impact:** Highlighted need to rethink pricing and discount strategy.

**2. High-Margin Products Drive Profit**

Sub-categories like **Copiers and Phones** consistently delivered strong profit margins.

**Impact:** Opportunity to prioritize these in marketing and inventory planning.

**3. Seasonal Sales Patterns**

Sales trends showed clear monthly and weekly fluctuations, indicating seasonality.

**Impact:** Supports better demand forecasting and campaign timing.

**4. Customer Concentration**

A small group of customers contributed disproportionately to revenue and profit.

**Impact:** Identified both:

* High-value customers (retention opportunity)
* Over-reliance risk

**5. Low Customer Retention Signals**

Most customers placed only a few orders, with limited repeat purchases.

**Impact:** Need for loyalty programs and retention strategies.

**6. Discounts Reduce Profitability**

Higher discounts often failed to translate into proportional profit gains.

**Impact:** Reinforces importance of controlled discounting.


## 📈 Business Impact

If implemented, these insights could help Osta Limited:

    * Increase profitability through smarter pricing
    * Improve customer retention and lifetime value
    * Optimize product portfolio
    * Align operations with demand trends
    * Reduce revenue dependency on a few customers


**🚀 Tools Used**
* Tableau (Dashboard Development)
* Excel / CSV (Data Source)

## 🧾 Conclusion

This project demonstrates how raw transactional 
data can be transformed into **actionable business insights** through 
effective data visualization and analysis. It highlights the importance
 of not just tracking revenue, but understanding **profitability,
 customer behavior, and trends over time.**

## 👤 Author

 Stanley Eric  

Business Intelligence Analyst | Data Analyst | Tableau Developer



