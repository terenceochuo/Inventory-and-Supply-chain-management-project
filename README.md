# Inventory-and-Supply-Chain-Management-Project

## Table of Contents

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tool used](#tool-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Data analysis](#data-analysis)
- [Insights](#insights)
- [Recommendations](#recommendations)
  
### Project Overview
This project demonstrates the application of Power BI in analyzing supply chain efficiency, cost optimization, and inventory performance. By integrating KPIs and interactive visuals, it helps businesses reduce excess stock, optimize lead times, and improve customer satisfaction.

### Data Source
Supply chain data:The primary dataset used for this analysis is the "Inventory_SupplyChain_Dataset.csv" file,containing detailed information of inventory held by the company
### Tool used
- Power BI - For data cleaning and visualization
### Data Cleaning and Preparation
In the initial preparation phase I loaded the data into power bi query editor where I formatted the date column from the text data type to date data type.The data had no more errors so i dived into the visualization part
### Data analysis 
I used the DAX functions in power bi to calculate the following metrics;
- Days Sales of Inventory (Measures the average number of days it takes for an organization to sells or use its entire inventory it has at the exposal).
  ```power bi
  Days sales of Inventory = DIVIDE(SUM(Inventory_SupplyChain_Dataset[Inventory Level]),SUM(Inventory_SupplyChain_Dataset[Cost of Goods Sold (COGS)]))*365
  ```
- Inventory Turnover Ratio (Measures how many times a company sells and replaces its inventory during a specific period (usually a year))
  ```power bi
  Inventory Turnover Ratio = DIVIDE(SUM(Inventory_SupplyChain_Dataset[Cost of Goods Sold (COGS)]),SUM(Inventory_SupplyChain_Dataset[Average Inventory]))
  ```
  -Warehouse Utilization %
  ```power bi
  Warehouse Utilization = DIVIDE(SUM(Inventory_SupplyChain_Dataset[Inventory Level]),SUM(Inventory_SupplyChain_Dataset[Warehouse Capacity]))
  ```
  These are some of the few keys KPIs that I visualized using the card.
### Insights
From the analysis here are some of the key Insights that I realized;
- Warehouse Utilization: 34.1%
  - The warehouse is underutilized (capacity used is low compared to available space). This may indicate inefficiency in space management or potential to optimize costs.

- Days Sales of Inventory (DSI): 16 days
  - On average, inventory stays in storage for only 16 days before being sold. This is relatively efficient and suggests good turnover.
    
- Inventory Turnover Ratio: 23.47
  - This is a very high turnover ratio, meaning inventory is being sold and replaced quickly. Strong sign of demand and efficient inventory management.

- Transportation Cost by Region and Category
  - Transportation costs are highest in the West region and lowest in the South.

- Units Sold by Year
  - Sharp growth trend after 2020 (from ~5K units to nearly 200K in 2024).This indicates strong market expansion and demand increase.

- Lead Time (Days) by Category
  - Accessories (16.6 days) have the longest lead time, while Clothing (15.29 days) has the shortest.Small differences, but reducing lead time could improve responsiveness.

- Backorder by Order Status
  - 838 fulfilled orders, 248 pending, 114 canceled.Although most orders are fulfilled, the pending and canceled orders highlight potential supply chain bottlenecks or demand-supply mismatches.

- Inventory Level by Category and Region
  - Clothing and Electronics have the highest inventory levels across most regions.

- Accessories hold relatively lower stock compared to others.Suggests stronger demand or stockpiling strategy for Clothing/Electronics.

### Recommendations
Here are precise recommendations based on the dashboard findings:
- Improve Warehouse Utilization – Optimize storage planning or consolidate facilities to reduce underutilization costs.
- Optimize Transportation Costs – Review routes and supplier contracts, especially in the West region, to cut logistics expenses.
- Reduce Lead Times – Strengthen supplier relationships and streamline procurement for Accessories and Electronics.
- Address Backorders – Enhance demand forecasting and inventory planning to reduce pending and canceled orders.
- Leverage Sales Growth – Align production and inventory strategies with rising demand to sustain growth without stockouts.

  
