
# MAVEN MARKET DATA ANALYSIS WITH POWER BI

## Introduction

This project is a part of assignment to the Microsoft Power BI Desktop for Business Intelligence (2023) course offered by Udemy on behalf of Maven Analytics.

## Project Overview

Maven Market, a fictitional multi-national grocery chain with locations in Canada, Mexico and the United States sought insights for their business by hiring a business intelligence analyst.

The management of Maven Market has intimated their expected dashboard contents for the year 1998 only. 
They would like the BI Analyst to track their KPIs sales, revenue, profit and returns, compare performance across regions, analyze weekly transaction trends, and track status of revenue target

The key steps involved in conducting a thorough analysis of the grocery store chain were as follows:


### Power Query (ETL)

The following ETL steps were undertaken to clean & transform the raw data into a meaningful and suitable dataset which is essential for an accurate analysis

1. Extracted CSV file into power query editor
2. Replace "null" values with zeros for easier calculations
3. Creating Calculated & Conditional columns
4. Use Group by to aggregate the data
5. Extracting the characters from field to a new coloumn
6. Check column distribution and column quality

### Model View

1. All relationships followed one-to-many cardinality, with primary keys on the lookup (Dimension) side and foreign keys on the data (Fact) side
2. Align tables in Star/Snowflake schema
3. Filter context flows "downstream" from lookup tables to data tables
4. Data tables are connected via shared lookup tables (not directly to each other)
5. Hide all Foreign keys so that we are filtering with proper columns in lookup tables

### DAX

Important DAX measures used for calculations are as follows:

1. Quantity Sold: Sum of quantity from Transaction table

2. Quantity Returned: Sum of quantity from Return table

3. Total Transactions: Counts number of rows from Transaction table.

4. Total Returns: Counts number of rows from Return table.

5. Return Rate: Counts number of rows from Transaction table.

6. All Transactions: Calculate grand total transactions, regardless of filter context.(used ALL function)

7. All Returns: Calculate grand total returns, regardless of filter context. .(used ALL function)

8. Total Revenue & Total Cost: calculate using ALL iterator function and RELATED lookup function

9. Total Profit: Total revenue minus total cost

10. Profit Margin: Divide total profit by total revenue

11. YTD Revenue: Calculate year-to-date total revenue using DATESYTD function

12. Last Month Transactions, Last Month Revenue, Last Month Profit, and Last Month Returns: Create measure using CALCULATE and DATEADD function

13. Revenue Target 5% lift over the previous month revenue

### Visualization

Data visualisation need utmost attention as it can be used to communicate to the audience only when presented in simple and meaningful way. 

I have used Matrix visuals to display 30 products details, their Profit, and Return % to understand which are the most popular and least popular products.

Tree Map to show the different grocery store regions and filter them and Map visual for better view of the regions.

I have used Gauge charts to monitor revenue growth from previous month (target) and KPI cards to display Total transactions, Profit and Returns.

### Key insights

1. Top performing band in sales - Hermanos

2. Top profit giving brand-Plato with 64.07% profit margin

3. The brand facing highest return of products- PigTail with 1.71%

4. The store in Hidalgo city, Mexico has recorded highest number of sales (16,614).It has sold products of Ebony brand for 730 times

5. The store in Portland, USA clocked 1000 Sales in December







