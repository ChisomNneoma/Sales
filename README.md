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


![Salesdb1.JPG](https://github.com/ChisomNneoma/Sales/assets/154308780/5f1a8ab7-9be4-43ad-bd7a-332dd2c64749)


Next is the Customer's demography report. All represented by charts.

- Top 5 active customers
- Top 10 profitable customers
- Preferred ship mode
- Top 5 states by profit
- Profit by customer segment




### Result of Analysis

The KPIs for the Sales Performance Report reveals:
- Total Sales as $470.53k
- Total Profit - 61.62k
- Total Orders - 2,102
- Profit Margin - 13.10%


1.Sales By Category reveals the top 3 product category with the highest sales as Furniture, Technology, and office supplies.

2. The second bar chart shows the top 10 products with the highest sales.

3. The region with the highest sales, also represented on a bar chart is the Eastern region.

4. A trend analysis showing monthly sales trend on a line chart reveals November as the month with the highest sales, followed by December. Right before November, the store experienced a sharp decline in Sales in October.
January also had the store experiencing low sales but sales picked up in March.

The Customer Demography Report was done to show the types of customers that patronizes the store, how frequently they visited the store, the products they purchased and how much they spent among other factors.

1.The KPIs reveal:

- The total number of customers that the store had - 573
- Total quantity of products sold - 7,979
- Total unique orders made by customers - 1038
- Average sales per customer - $821.2

2. A column chart was used in revealing the top 5 active customers. This shows the number of visits these customers made to the store over the year.

3. Top 10 profitable customers is shown on a bar chart. This reveals the customers that spends the most amount of money.

4.Profit by customer segment is displayed on a doughnut chart. This shows the 3 segments of customers based on the type of products they purchase, and the number of customers under each segment with the Corporate segment leading with 47.64%.

5. Top 5 states by profit reveals California as the state with highest sales at $88k , while New York has the highest profit of $19k.



### Findings

From the sales performance analysis, I discovered that

1. The product category with the highest sales is Furniture, but the product with the highest sales is not a furniture but a technology product.

2. There is more sales activity in November and December but significantly low sales in January. Could this be as a result of the festivities in the end of the year?
Why was there a sharp decline in sales in October?

3. The active customers are different from high spending customers. Further explaining that it's not about the frequency of a customer that determines the customers that spends more money in the store.

4. Region with the highest sales is not necessarily a determinant to states with the highest profit.
The region that brought in the highest sale is Eastern region, the state with the highest sales is California, not an Eastern state, while New York, an Eastern state raked in the highest profit.

5. Customers purchase more products in the Corporate segment compared to consumers segment.


### Recommendations

1. Despite Furniture having the highest sales, prioritize showcasing and promoting technology products since they contribute significantly to overall sales. 

2. Plan marketing and promotions around the holiday season to capitalize on increased sales activities in November and December.
Implement targeted promotions or events in January to counter traditional sales dip after the holiday season. Special offers and new products should be introduced to encourage more sales in the first quarter of the year. For example, Valentine and Easter promotions should kick in immediately after the holidays.

3. Tailor marketing strategies differently for active customers versus high spending customers.
Loyalty programs should be considered for high spending customers.

4. Adjust marketing and pricing strategies in states with high sales and low profit margin. Prioritize states with higher profit margin over those with only high sales. Evaluate factors affecting profitability in different states and optimize accordingly.

5. Consider strategies to boost sales in the Consumer products segment. This could be targeted marketing or product offerings catering to consumer needs.

### View Dashboard

To view and interact with dashboard on Power BI,

[Click here](https://app.powerbi.com/view?r=eyJrIjoiOWJmZmIwMDYtM2ZjOS00NDRmLThjZDEtMWJmMmY3OWEyZjI4IiwidCI6IjY4NGU3NTM1LWJlODEtNDQ0Yi05ZWMwLWNjZWYzMDQxYTQyNiJ9)

Navigate pages using bookmarks


