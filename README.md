# Coffee-Production-Sales-Analytics-Dashboard_Power-BI
Scope & Goal: Developed an end-to-end Power BI solution to monitor the coffee-bean supply chain—tracking daily production, monthly output, inventory levels, and sales rate—so managers could quickly spot bottlenecks, excess stock, and demand spikes.
Step-by-Step Analysis Process
1. Understanding Business Problem
Objective: Analyze coffee production, sales, and inventory data to identify trends, imbalances, and decision-making opportunities.

Key questions:

Which bean types are overproduced or underperforming?

Are sales aligned with production?

How much inventory is moving each month?

2. Data Collection
Data sources:

Daily table – daily production volumes by bean type.

Monthly table – monthly summaries of production and inventory.

InventSale table – inventory levels vs. sales volumes by product.

Each file contained relevant fields such as Date, Bean Type, Produced Units, Sold Units, and Inventory.

3. Data Cleaning & Preparation (Power Query)
Removed nulls, fixed data types (e.g., dates, integers).

Merged/normalized tables to ensure consistency.

Created custom columns like:

Month-Year for time series analysis.

Calculated fields to compute metrics such as:

Total Production

Inventory Carry Forward

Sales Units

4. Data Modelling
Designed star schema:

Fact Table: Merged data of Production + Sales + Inventory.

Dimension Tables: Date, Product/Bean Type.

Established relationships using primary/foreign keys (e.g., DateID, BeanID).

5. KPI Development (DAX)
Built DAX measures to answer key business queries:

Total Production = SUM(Daily[Produced Units])

Total Sales = SUM(InventSale[Sold Units])

Inventory Days = DIVIDE([Inventory Units], [Daily Avg Sales])

MoM Sales Change = (Current Month - Previous Month Sales) / Previous Month Sales

6. Dashboard Design
Created 3 analytical report pages:

Daily Report: Line charts showing daily production trends by bean type.

Monthly Summary: Combo charts (production vs. sales), slicers for bean type and month.

Inventory vs Sales: Scatter chart showing excess stock or sales gaps.

Features added:

Tooltips, slicers, filters, bookmarks

Clean color theme for visual consistency

