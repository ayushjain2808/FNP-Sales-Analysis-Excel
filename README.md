📊 Ferns N Petals Sales Analysis Dashboard (Excel)
An end-to-end data analysis project for "Ferns N Petals," an online gifting company, leveraging advanced Microsoft Excel functionalities to transform raw sales data into actionable business insights and an interactive dashboard.
________________________________________
✨ Project Overview
This project demonstrates a comprehensive data analysis workflow within MS Excel, from raw data ingestion and cleaning to advanced modeling, insightful analysis, and dynamic dashboard creation. The primary goal was to provide Ferns N Petals with a clear, interactive view of their sales performance, enabling data-driven decision-making.
________________________________________
🚀 Key Features & Technologies Used :

This project showcases proficiency in a wide array of essential Excel tools and data analysis concepts:

•	Data Extraction & Transformation (ETL):
o	Power Query Editor: Utilized for efficient data loading from a folder (handling multiple CSVs), robust data cleaning (e.g., handling data types, removing irrelevant columns), and complex data transformations (e.g., extracting date/time components, calculating delivery durations).

•	Data Modeling:
o	Power Pivot: Employed to build a robust Star Schema data model, establishing one-to-many relationships between Fact (Orders) and Dimension (Customers, Products) tables.

•	Advanced Calculations:
o	DAX (Data Analysis Expressions): Used to create calculated columns (e.g., Revenue, Day Name) within the Power Pivot data model for enhanced analytical capabilities.

•	Data Analysis & Visualization:
o	Pivot Tables: Generated dynamic summaries to answer specific business questions.
o	Pivot Charts: Created various chart types (Bar, Line) for compelling visual representation of trends and comparisons.
o	Slicers: Implemented interactive filters for dynamic exploration of data by Occasion.
o	Timelines: Added interactive date filters for granular analysis across time periods.

•	Statistical Analysis:
o	CORREL Function: Applied to assess the relationship between Order Quantity and Delivery Time.
•	Dashboard Design:
o	Created a user-friendly, interactive dashboard integrating KPIs, charts, and filters for a holistic view of sales performance.

________________________________________
📂 Dataset Overview
The analysis is based on three interconnected CSV files, representing key aspects of Ferns N Petals' operations:
•	customers.csv: Contains customer demographics (Customer ID, Name, City, Gender, Contact, Email, Address).
•	orders.csv: The central Fact Table, detailing each order (Order ID, Customer ID, Product ID, Quantity, Order Date/Time, Delivery Date/Time, Location, Occasion).
•	products.csv: Provides product details (Product ID, Product Name, Category, Price, Occasion, Description).
________________________________________
🎯 Problem Statement & Business Questions Addressed
The project aimed to answer critical business questions to provide actionable insights into sales performance:
1.	Total Revenue: Identify the overall revenue generated.
2.	Average Order and Delivery Time: Calculate the average time taken for orders to be delivered.
3.	Monthly Sales Performance: Examine how sales fluctuate across different months.
4.	Top Products by Revenue: Identify the highest-earning products.
5.	Customer Spending Analysis: Understand the average order value per customer.
6.	Sales Performance by Top Categories: Analyze revenue contribution from different product categories.
7.	Top 10 Cities by Number of Orders: Pinpoint cities with the highest order volumes.
8.	Order Quantity vs. Delivery Time: Analyze if higher order quantities impact delivery times using correlation.
9.	Revenue Comparison by Occasions: Compare revenue generated across various gifting occasions.
10.	Product Popularity by Occasion: Identify which products are most popular during specific occasions.
11.	Order Patterns by Hour/Day: Analyze preferred ordering times/days for targeted marketing.
________________________________________
🛠️ Methodology & Project Phases
The project followed a structured data analysis pipeline:
1.	Data Extraction:
o	Utilized Power Query Editor's "From Folder" feature to import all three CSV files simultaneously, ensuring future scalability for new data.
2.	Data Cleaning & Transformation:
o	products: Removed irrelevant 'Description' column.
o	customers: Converted 'Contact Number' to 'Text' to preserve formatting.
o	orders:
	Extracted Month Name, Order Hour, and Delivery Hour from date/time columns using "Add Column" in Power Query.
	Calculated Delivery Difference (Days) by subtracting Order Date from Delivery Date.
	Performed a Left Outer Merge (Join) with the products table on Product ID to bring Price into the orders table, essential for revenue calculation.
	Ensured correct data types across all columns.
3.	Data Loading:
o	Loaded the transformed data from Power Query directly into Excel's Data Model, enabling multi-table analysis.
4.	Data Modeling (Power Pivot):
o	Enabled Power Pivot Add-in.
o	In Power Pivot Diagram View, established One-to-Many relationships:
	Customers[Customer ID] ➡️ Orders[Customer ID]
	Products[Product ID] ➡️ Orders[Product ID]
o	This created a Star Schema, optimizing for efficient querying.
5.	Advanced Calculations (DAX):
o	Created a Revenue calculated column in the Orders table: Revenue = [Quantity] * [Price].
o	Created a Day Name calculated column in the Orders table: Day Name = FORMAT([Order Date], "DDDD").
6.	Data Analysis (Pivot Tables & Formulas):
o	Generated multiple Pivot Tables from the Data Model to answer each business question.
o	Applied Value Filters (e.g., Top 5, Top 10) and custom sorting (e.g., chronological month order).
o	Used the CORREL function in Excel to statistically analyze the relationship between Order Quantity and Delivery Time, finding a weak positive correlation (0.3478).
7.	Dashboard Creation & Interactivity:
o	Designed a dedicated "Dashboard" sheet.
o	Inserted Pivot Charts (Bar, Line) for each key insight.
o	Integrated Slicers (for Occasion) and Timelines (for Order Date) and connected them to all relevant Pivot Tables using Report Connections for dynamic filtering.
o	Displayed key KPIs (Total Orders, Total Revenue, Average Order-to-Delivery Time, Average Customer Spending) using shapes linked to Pivot Table values.
o	Applied consistent formatting and branding (FNP logo, theme colors) for a professional look.
8.	Executive Summary:
o	Utilized AI (ChatGPT/Gemini) to draft a concise executive summary, highlighting key insights and actionable recommendations derived from the dashboard.
________________________________________
💡 Key Insights & Outcomes
The interactive dashboard provides the following critical insights:
•	Revenue Peaks: Significant revenue spikes observed during major gifting occasions like Rakshabandhan, Anniversary, Diwali, and Holy.
•	Average Delivery: Orders are delivered, on average, within ~5-6 days.
•	Top Performers: Identified top-selling products and categories (e.g., 'Colors' during Holi, 'Sweets' generally) and top contributing cities.
•	Ordering Patterns: Revealed peak ordering times (e.g., 7-8 PM, surprisingly 6 AM), valuable for targeted marketing campaigns.
•	Customer Spending: Average customer spending per order is approximately ₹3,520.
•	Quantity vs. Delivery: A weak positive correlation suggests that while higher quantities might slightly increase delivery time, it's not a dominant factor.
________________________________________
📈 Dashboard Preview
<img width="1650" height="635" alt="Screenshot 2025-07-26 220022" src="https://github.com/user-attachments/assets/020c89a5-33ba-4286-9b09-1efc08f90f34" />

