# Sales Insights Report

## Problem Statement 
In this project I have created an interactive Power BI dashboard to unlock sales insights that are not visible before sales team for decision support and automate them to reduce manual time spent in data gathering.
This dashboard provides quick and latest sales insights in order to support data driven decision making.

### Data preview
This dataset consists of five schemas:
-  Customers: It stores information related to customers like their name, type and this schema has a unique id 'customer_code' that is the primary key
-  Transactions: It stores information related to all the transactions happening with the company's customers, like the id of the product sold, customer_code, sales_amount etc
-  Products: It stores information related to the products sold by the company, product_code is it's primary key
-  Markets: It stores information related to the market name and the zone in which their customers are located, markets_code is it's primary key
-  Date: It stores information related to the dates on which the transactions happen

After performing data modelling, I have established relations between the table and represented them in the start schema approach
![Dataset Schema](Star_schema.png)


### Steps followed
1.  Load data (.sql file) into MySQL Workbench, perform basic data analysis
2.  Load the sql data file in PowerBI desktop
3.  Performed data modelling, established relationships between the tables using the star schema approach
4.  Performed data cleaning and ETL in Power Query Editor:
  -  Removed rows having blank and non positive values in the 'Zone', 'Sales'columns
  -  Removed duplicate records to maintain data quality
  -  Added a column using conditional column in PowerBI, the new column would have sales quantity all represented in a single currency(Rs)
5. After completing ETL, built the dashboard using PowerBI dashboard:
  - Created new measures, Revenue and Sales Qty, displayed them using cards in PowerBi
  - Plotted a bar chart that shows distribution of revenue by markets
  - Plotted another bar chart that shows distribution of sales quantity by markets
  - Created multiple slicers that will avail the user to view all the data visuals by the year, month selected
  - Using a bar chart displayed the top 5 customers that generate the most revenue, using filters.
  - Also displayed the top 5 products that generate the most revenue
  - Plotted a revenue trend, revenue by month

    
![Sales Report](Sales_report.png)


### Insights 
1.  Revenue Contribution by Market:
-   The Delhi NCR market is the top-performing market, contributing the largest share to revenue (₹519.51M), while other markets like Mumbai and Ahmedabad contribute significantly less. Markets like Bengaluru and Bhubaneswar show negligible contributions, which could indicate untapped opportunities or areas needing improvement.
  
2.  Sales Quantity by Market:
-  Similar to revenue, Delhi NCR dominates sales quantity, indicating both high customer engagement and a strong market presence. Lower sales in other regions, such as Nagpur and Bengaluru, highlight potential markets for expansion or targeted campaigns.

3.  Revenue Trends:
-  The monthly revenue trend shows notable fluctuations, with peaks occurring around certain periods (e.g., mid-2018 and late-2019). This could align with seasonal demands, special promotions, or other market trends. The drop at the end of the timeline may indicate declining performance that warrants further investigation.

4.  Top Customers:
-  The top customer, Electricalsara Stores, contributes ₹413.33M, a substantial portion of the total revenue. Focusing on maintaining strong relationships with such key accounts is vital for sustaining revenue streams.

5.  Top Products:
-  A product labeled as "(Blank)" contributes significantly to revenue (₹468.96M), which might suggest a data quality issue or mislabeling. This needs immediate attention for proper reporting and decision-making.
Other top-performing products like Prod040 and Prod159 are consistent revenue drivers and could be leveraged for targeted marketing efforts.

### Conclusion
The interactive dashboard successfully unlocks key sales insights, providing a comprehensive view of market performance, revenue trends, and top contributors (products and customers). This automation significantly reduces manual effort in data collection and processing, empowering the sales team to make data-driven decisions swiftly.
