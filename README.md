# Coffee-Production-Sales-Analytics-Dashboard_Power-BI:

## Scope & Goal: 
Developed an end-to-end Power BI solution to monitor the coffee-bean supply chain—tracking daily production, monthly output, inventory levels, and sales rate—so managers could quickly spot bottlenecks, excess stock, and demand spikes.

 ### Objective: 
 Analyze coffee production, sales, and inventory data to identify trends, imbalances, and decision-making opportunities.

## Key questions:

1. Which bean types are overproduced or underperforming?

2. Are sales aligned with production?

3. How much inventory is moving each month?

 ## Data Collection

1. Daily table – daily production volumes by bean type.

2. Monthly table – monthly summaries of production and inventory.

3. InventSale table – inventory levels vs. sales volumes by product.

### Each file contained relevant fields such as Date, Bean Type, Produced Units, Sold Units, and Inventory.

 ## Data Cleaning & Preparation (Power Query)
1. Removed nulls, fixed data types (e.g., dates, integers).

2. Merged/normalized tables to ensure consistency.

3. Created custom columns like:

4. Month-Year for time series analysis.

5. Calculated fields to compute metrics such as:

6. Total Production

7. Inventory Carry Forward

8. Sales Units

## Data Modelling
1. Designed star schema:

2. Fact Table: Merged data of Production + Sales + Inventory.

3. Dimension Tables: Date, Product/Bean Type.

4. Established relationships using primary/foreign keys (e.g., DateID, BeanID).

## KPI Development (DAX)
### Built DAX measures to answer key business queries:

1. Total Production = SUM(Daily[Produced Units])

2. Total Sales = SUM(InventSale[Sold Units])

3. Inventory Days = DIVIDE([Inventory Units], [Daily Avg Sales])

4. MoM Sales Change = (Current Month - Previous Month Sales) / Previous Month Sales

## Dashboard Design
### Created 3 analytical report pages:

1. Daily Report: Line charts showing daily production trends by bean type.

2. Monthly Summary: Combo charts (production vs. sales), slicers for bean type and month.

3. Inventory vs Sales: Scatter chart showing excess stock or sales gaps.

## Features added:

1. Tooltips, slicers, filters, bookmarks

2. Clean color theme for visual consistency

