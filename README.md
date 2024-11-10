# LITA-CAPSTONE-PROJECT

## Project Title: Sales Performance Analysis for a Retail Store

### Table of Contents
[Project Overview](#project-overview)

[Dataset](#dataset)

[Data Sources](#data-sources)

[Analytical Tools Used](#analytical-tools-used)

[Data Cleaning](#data-cleaning)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)

[Insights](#insights)

[Recommendation](#recommendation)

### Project Overview
This project aims to analyse the sales data of a retail store to gain insights into customer purchasing behaviour, product performance, regional and monthly sales trends in order to make business decisions.

### Dataset
The dataset contains the following columns:
- OrderID: A unique identifier for each order
- CustomerID: A unique identifier for each customer
- Product: The specific product purchased
- Region: The geographical location of customers
- Order Date: The date the order was placed
- Quantity: The number of units purchased for each product in an order
- Unit Price: The price per unit of a product
- Sales: The sales value for an order, calculated as Quantity * Unit Price

  ### Data Sources
The primary source of data used here is Sales Data.csv and this is an open source data that can be downloaded from an open source online such as Kaggle or FRED, though this dataset was given by the Incubator Hub(LITA).

### Analytical Tools Used
The analytical tools used were:
- MsExcel- this was used for data cleaning and analysis
- SQL (Structured Query Language)- this was used to query data
- Power BI- this business intelligence tool was used for data visualization

  ### Data Cleaning
In this phase of my analysis, i performed the following actions:
- Data loading: Loaded the data
- Blank Value Check: Verified the dataset for blank values
- Data Type Conversion: Converted specified columns to text format for consistency
- Data Standardization: Reformatted date columns to YYYY-MM-DD for uniformity
- Duplicate Removal: Removed duplicate rows to ensure unique records. 40,079 duplicates were found and removed left with 9,921 unique values out of 50,000 records given.

  ### Exploratory Data Analysis
  In this phase of my analysis, the dataset was explored to answer questions such as:
  - Which product had the most sales?
  - What is the regional sales trend?
  - What is the monthly sales performance?
    
### Data Analysis
- Excel Analysis
   - Average Sales per Products
  ```Excel
  =AVERAGEIF(C:C,"shirt",H:H)
  =AVERAGEIF(C:C,"Shoes",H:H)
  =AVERAGEIF(C:C,"Gloves",H:H)
  =AVERAGEIF(C:C,"Hat",H:H)
  =AVERAGEIF(C:C,"Jacket",H:H)
  =AVERAGEIF(C:C,"Socks",H:H)
  ```
   - Total Revenue by Region
  ```Excel
  =SUMIF(D:D,"South",H:H)
  =SUMIF(D:D,"East",H:H)
  =SUMIF(D:D,"North",H:H)
  =SUMIF(D:D,"West",H:H)
  ```
- SQL Queries
  - Total Sales per Products
  ```SQL
  Select Product, SUM(Sales)as Totalsales
  from [dbo].[Sales Data_Project]
  group by Product
  order by Totalsales desc
  ```
  - Sales Transactions by Region
  ```SQL
  Select Region, COUNT (OrderID) as Transaction_COUNT
  from [dbo].[Sales Data_Project]
  group by Region
  order by Transaction_COUNT desc
  ```
  - Highest Selling Product
  ```SQL
  Select top 1 Product, SUM(Sales) as Totalsales
  from [dbo].[Sales Data_Project]
  group by product
  ```
  
  ### Data Visualization
 ![SALES PIVOT TABLE](https://github.com/user-attachments/assets/030a76c6-2f3c-44e8-91e4-b3213257dd90)


 ![SALES POWER BI](https://github.com/user-attachments/assets/fca76fd6-a29e-457c-83b3-0e37d8c64fac)

### Insights
The total revenue of Everything Wears Boutique from January, 2023 to August, 2024 is $2 million which cuts across the four regions( North, South, East and West), generated from the sales of the six products ( shoes, shirts, hat, gloves, jacket and socks).

The best performing product is the shoes accounting for over 29.2% of revenue generated followed by shirt, 23.1%. Hats and gloves being the mid performing products produced 15.1% and 14.1% respectively. The least performing products are the jackets and socks which generated only 9.9% and 8.6% respectively.

Geographically, the South Region has emerged as the highest selling region with 44.2% of total revenue while East and North regions have recorded lower sales producing 23.1% and 18.4% of total revenue respectively. West region being the least performing region recorded a production of 14.3% of total revenue generated. This disparity suggests opportunities for market expansion and targeted marketing strategies.

These findings highlight areas of strength and potential growth, providing valuable insights for future business strategies and resource allocation.

### Recommendation
- Sales Strategy
  - The South region was able to produce 44.2% of total revenue with the sales of only three products (shoes, gloves, socks) during the time under review. Thus, more products (shirt, hat, jacket) should be allocated to this region for sales growth.
  - More focus should be looked into the products that drives sales growth. In this review, i found out that the top 3 products that were sold in quantity are the shoes, hat and shirt. I'll recommend a customer market research should be done to analyse customer feedback. This will enable Capstone Retail Store to serve their customers better.
- Product Optimization
  - Shoes has the highest sales revenue. Therefore, there should be increased production and marketing efforts for shoes
  - Products like shirt, hats, gloves, jackets and socks have high growth potential. Thus, product offerings should be expanded and there should be marketing campaigns for these products.
- Regional Focus
  - The West Region has the lowest sales. Therefore, we should conduct market research to identify opportunities for growth.
