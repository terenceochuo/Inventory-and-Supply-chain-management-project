# Inventory-and-Supply-Chain-Management-Project
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
### Results/Findings
From the analysis here are some of the key Insights that I realized;
- Warehouse Utilization: 34.1%
  - The warehouse is underutilized (capacity used is low compared to available space). This may indicate inefficiency in space management or potential to optimize costs.

- Days Sales of Inventory (DSI): 16 days
  - On average, inventory stays in storage for only 16 days before being sold. This is relatively efficient and suggests good turnover.
    
- Inventory Turnover Ratio: 23.47
  - This is a very high turnover ratio, meaning inventory is being sold and replaced quickly. Strong sign of demand and efficient inventory management.

  
