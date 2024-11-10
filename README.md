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
