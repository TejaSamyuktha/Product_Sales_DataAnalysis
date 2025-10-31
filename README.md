Product-Sales-Data Analysis Dashboard

## Table of Contents

- [Case Study](#case-study)
- [Dataset Description](#dataset-description)
- [Data Analysis](#data-analysis)
- [Dashboard](#dashboard)


## Case Study
The objective of this case study is to analyze *Product Sales performance* by tracking total orders, total profit, total sales, and total units sold.  
The dashboard provides a comprehensive overview of *sales trends, regional contributions, and top-performing locations*, helping businesses identify growth opportunities and performance gaps.


## Dataset Description

This dataset contains detailed information on *sales transactions, **products, **retailers, **regions, and **sales methods* used in distributing sports products.  
It enables analysis of total sales, profitability, and performance across various geographies and channels.

Below are the key tables and their fields:

---

### *Region*
- *regionid* – Unique identifier for each region.  
- *city* – City where the sales took place.  
- *state* – State or province corresponding to the city.  

> Helps in analyzing sales performance by geography (city/state level).

---

### *Products*
- *pid* – Unique product identifier.  
- *product* – Name of the product (e.g., Football, Tennis Racket, Sports Shoes).  

> Provides details of the products sold in each transaction.

---

### *Retailer*
- *retailerid* – Unique retailer identifier.  
- *retailer* – Name of the retailer or store.  

> Identifies which retailer sold the product, allowing for retailer-level performance comparison.

---

### *SalesMethod*
- *salesmethodid* – Unique identifier for each sales method.  
- *salesmethod* – Type of sales method (e.g., Online, In-Store, Distributor).  

> Used to analyze performance by sales channel or method of transaction.

---

### *SportsProducts* (Fact Table — transactional level)
- *invoiceid* – Unique identifier for each sales transaction.  
- *retailerid* – Key linking to the *Retailer* table.  
- *productid* – Key linking to the *Products* table.  
- *regionid* – Key linking to the *Region* table.  
- *salesmethodid* – Key linking to the *SalesMethod* table.  
- *price_per_unit* – Selling price per individual unit.  
- *units_sold* – Total number of units sold in the transaction.  
- *total_sales* – Total revenue generated (price_per_unit × units_sold).  
- *operating_profit* – Profit earned after deducting operating expenses.  
- *operating_margin* – Profitability ratio (operating_profit ÷ total_sales).  




## 📋 Table of Contents
- [DAX Measures for Power BI](#dax-measures-for-power-bi)
  - [• Total sales](#•-total-sales)
  - [• Total orders](#•-total-orders)
  - [• Total Profit](#•-total-profit)
  - [• Units Sold](#•-Units-Sold)

---

DAX Measures for Power BI
### 1.Total sales
            Total Sales = SUM(SportProducts[Total Sales])
### 2.Total orders
           Total Orders = COUNT(SportProducts[Invoice Date])
### 3.Total Profit
            Total Profit = SUM(SportProducts[Operating Proft])
### 4.Units Sold
          Units Sold = SUM(SportProducts[Units Sold])
            
            
            






## Data Analysis
### 1.   Sales by Quarter and Region
Insight:
Quarterly analysis shows consistent growth throughout the year, with Southeast and Northeast regions leading in total revenue.
### 2.  Regional Sales Contribution
Insight:

The Southeast region contributes nearly 27% of the total sales, followed by the South and Midwest.
This insight helps identify high-performing areas and potential growth zones
### 3. Top 10 Locations
Insight:

New York and California dominate the top 10 list, contributing the highest sales volume.
The top states show a healthy balance of online and in-store sales.
### 4.Product Sales by Month
Insight:

Sales remain stable with visible growth in Q2 and Q4, suggesting seasonal demand fluctuations.
These insights can help plan promotional campaigns more effectively.

## Dashboard


<img width="1920" height="1019" alt="product-sales-data-analysis-dashboard" src="![product_sales_dataanalysis_img](https://github.com/user-attachments/assets/81f049ac-9f20-4a7a-b3e2-887ea475a12f)
" />


