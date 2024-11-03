# LITA_CAPSTONE_PROJECT-1

### Table of Content
---
1. [Project Overview](#project-overview)
2. [Introduction](#introduction)
3. [Tools Used](#tools-used)
4. [Data Exploration](#data-exploration)
5. [SQL Queries](#sql-queries)
6. [PowerBI Dashboard](#powerbi-dashboard)
7. [Insights and Recommendations](#insights-and-recommendations)
8. [Conclusion](#conclusion)
9. [Appendices](#appendices)

### Sales Performance Analysis for LITA Capstone Retail Store
---
### Project Overview
---
This project shows the analysis of the sales performance of LITA Capstone retail store. The analysis was carried out by exploring the sales data to uncover key insights such as top-selling products, regional performance, and monthly sales end.

### Introduction
---
LITA Capstone retail store, a leading retail chain with multiple locations across the region, seeks to optimize its sales performance and improve customer engagement. With increasing competition in the market, the store's management recognizes the need for data-driven decision-making to stay ahead.

- Problem Statement: 
The store's current sales analysis process is manual, time-consuming, and limited in scope. The management team lacks a comprehensive understanding of sales trends, product performance, and regional variations, hindering strategic decision-making.

- Project Objectives
  1. Analyze sales data to identify key insights such as top-selling products, regional performance, and monthly sales trends.
  2.   Develop a data driven framework for sales performance evaluation.
  3.   Provide actionable insights to inform product optimization, regional sales strategies, and customer engagement initiatives.

- Business Goals
  1. Increase overall sales revenue by 10% within next quarter.
  2. Improve product mix and optimize inventory management.
  3. Enhance customer satisfaction and loyalty through targeted marketing initiatives.
  4. Strengthen competitive positioning through data-driven decision-making.

- Dataset Description:
  The project utilizes a comprehensive sales dataset spanning [January 2023 -December 2024], encompassing:
  - Sales transactions.
  - Product Information
  - Customer demographics
  - Regional data
  - Sales dates and times

### Tools Used
---
This project employs a combination of data exploarion, SQL querying, and data exploration, SQL querying, and data visualization technqiues using:
- Microsoft Excel for data exploration and calculation
- SQL Server for data querying and analysis
- PowerBI for interactive dashboard creation

### Data Exploration
---
- EXCEL PIVOT TABLE AND CHARTS Total sales by product
   - Total sales by product.
   - Total sales by region.
   - Total sales by month.
     
- Calculated metrics:
   - Average sales per product.
   - Total revenue by region.
 
### SQL Queries
---
Query 1: Total sales by Product Category.
```SQL
SELECT * FROM [dbo].[LITA Capstone Datasets]
SELECT Product,SUM(Quantity)
as Total_Sales
FROM [LITA Capstone Datasets]
GROUP BY Product
```
Query 2: Number of Sales Transactions by Region
```SQL
SELECT Region,SUM(Quantity)
as Total_Sales
FROM[LITA Capstone Datasets]
GROUP BY Region
```
Query 3: Highest-selling Product by Total Sales Value
```SQL
SELECT Product,SUM(Quantity)
as Total_Sales
FROM[LITA Capstone Datasets]
GROUP BY Product
Order By Total_Sales Desc
```
Query 4: Total Revenue per Product
```  SQL
SELECT Product,SUM(Quantity*UnitPrice)
as Total_Revenue
FROM[LITA Capstone Datasets]
GROUP BY Product
```
Query 5: Monthly Sales Totals for Current Year
```SQL
SELECT OrderDate,
SUM(Quantity) as Total_Sales
FROM [dbo].[LITA Capstone Datasets]
WHERE OrderDate = 2024
GROUP BY OrderDate
```
Query 6: Top 5 Customers by Total Purchase Amount
```SQL
SELECT Top 5
Customer_Id, SUM(Quantity) AS Total_Purchase
FROM [dbo].[LITA Capstone Datasets]
GROUP BY Customer_Id
ORDER BY Total_Purchase DESC
```
QUERY 7: Percentage of Total Sales by Region
```SQL
SELECT Region, SUM(Revenue)/SUM(Quantity)*0.1 AS Percentage_of_Total_Sales
FROM [dbo].[LITA Capstone Datasets]
GROUP BY Region
ORDER BY Percentage_of_Total_Sales
```
Query 8: Products with No Sales in Last Quarter
```SQL
SELECT Product,SUM(Quantity) AS Sales
FROM [dbo].[LITA Capstone Datasets]
WHERE MONTH(OrderDate)
BETWEEN 10 AND 12
GROUP BY Product
HAVING SUM(Quantity)=0
```
### PowerBI Dashboard
---
- Dashboard screenshots:
   - Sales overview
   - Top-performing Products
   - Regional Breakdown
- Description of visualizations and insights.

### Insights and Recommendations
---
Insights:
1. Product Performance
    - Top-selling products:
       - Hats
       - Shoes
       - Gloves
       - Shirt
2. Regional Sales Trends
    - Regions with highest sales revenue: East(102500) and South(122500)
    - Regions with lowest sales revenue: North(62500) and West(57500)

Recommendations:
- Short-Term (0-6 months):
  1. Product Optimization
      - Discontinue underperforming products
      - Increase inventory of top-selling products
      - Introduce new products in high-growth categories
  2. Regional Sales Strategies
      - Allocate targeted marketing budgets to high-growth regions.
      - Adjust pricing strategies for regions with low sales revenue.
      - Enhance customer engagement initiatives in key regions.

- Medium Term (6-18 months):
  1. Sales Channel Optimization
      - Invest in e-commerce platform enhancements
      - Optimize online/offline channel integration
      - Explore new sales channels (e.g; socail media, marketplaces)
        
  2. Data-Driven Decision-Making
     - Establish regular sales data analysis and reveiw processes
     - Devlop predictive analytics capabilities
     - Integates sales data with other business functions(e.g;marketing, supply chain)
   
- Long-Term (18+ months):
1. Strategic Partnerships
    - Explore partnerships with complementary businesses
    - Develop strategic relationships with key suppliers
    - Investigate opportunities for expansion into new markets
      
2. Innovative Sales Strategies
   - Explore emerging sales channels (e.g;AR/VR, social commerce)
   - Develop innovative sales formats (e.g; subscription services)
  
### Conclusion
---
This sales performance analysis project has provided valuable insights into LITA Capstone Retail Store's sales trends, product performance, regional variations, and customer bahviour, SQL querying, and data visualization techniques, we have identified opportunities for growth, optimization, and improvement.
 - Key Takeaways
   1. Data-driven decision-making is crucial for retail success.
   2. Product optimization and regional sales strategies can drive revenue growth.
   3. Customer engagement and retention are critical for long-term success.
   4. Emerging sales channels and innovative strategies can foster competitive advantage.

  - FINAL THOUGHT:
     This project demonstrates the power of data analysis in driving business growth and improvement.By embracing data-driven decision-making, LITA Capstone Retail Store can unlock new opportunities, drive innovation, and maintain a competitive edge in the retail market.

### Appendices
---
- Capstone Sales Dataset
