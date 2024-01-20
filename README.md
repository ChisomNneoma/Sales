# Super Store Sales Analysis

### Project Overview

This data analysis project aims to provide insight into the monthly sales performance of a Super Store for the period of one year. By analyzing various aspects of the sales data, I aim to identify trends, gain deeper understanding of the store's performance, and make data driven recommendations.

### Data Source

Dataset was provided as a zipped file which was unzipped and cleaned on Excel. I picked and worked with the month of January to create the dashboard on Power BI first before importing other months.

### Tools
- Excel - Data Cleaning
- Power BI
   - DAX for analysis and creating calculated measures
   - Data Modelling
   - Creating Report


### Exploratory Data Analysis

EDA involved exploring the sales data to answer questions such as

- What are the highest selling products?
- When is the peak sales priod?
- What are the total orders, total sales amount, total profit and profit margin?


### Data Analysis
This is a two page report. the first page shows the sales analysis for the store while the second page focused on the customer's demography.

I used DAX for data analysis in Power BI

1. Total Sales
   ```DAX
   
   SUM('Sales Folder FACT'[Sales])
   ```
2. Profit Margin
   ```DAX

   DIVIDE('Calculations'[Total Profit], 'Calculations'[Total Sales])
   ```
3. Time Intellignce - This sums up sales for the previous month, making it easier for the next month to be added and calculated automatically without having to repeat what was done all over again when a new data is added.
```DAX

Sales Previous Month = CALCULATE(SUM('Sales Folder FACT'[Sales]), PREVIOUSMONTH('Calendar DIM'[Date]))
```




Next is the Customer's demography report. All represented by charts.

- Top 5 active customers
- Top 10 profitable customers
- Preferred ship mode
- Top 5 states by profit
- Profit by customer segment

  

