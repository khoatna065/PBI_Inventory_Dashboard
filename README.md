# PBI_Inventory_Dashboard
Using SQL and PowerBI

# I. Introduction

## 1. Business question

AdventureWorks database supports standard online transaction processing scenarios for a fictitious bicycle manufacture - Adventure Works Cycles. 

The Warehouse Department is responsible for storing goods including product, semi-finished product, and raw materials for production. 

Warehouse managers and warehouse staff need to closely monitor and control the amount of goods in the warehouse, ensuring goods are stored at prescribed levels. From there, build appropriate strategies to better manage and operate storage activities. 

The Sales Department and Marketing Department also want to know the overview of inventory status to build, control, and adjust sales and marketing campaigns accordingly. 

## 2. Dataset

Dataset: AdventureWorks2019 (public Google BigQuery dataset)

Data dictionary: Please reach file "Data Dictionary" attached above

Dataset access:

- Log in to your Google Cloud Platform account and create a new project.
- Navigate to the BigQuery console and select your newly created project.
- In the navigation panel, select "Add Data" and then "Star a project by name".
- Enter the project name "adventurework2019"

# II. Process

## 1. Extract Data

- Total of produced quantity and total sold quantity by month/year/quarter (Fact_product table)

![alt](https://github.com/khoatna065/PBI_Inventory_Dashboard/assets/167158955/6bd0399d-c42d-4333-b169-375e64ed0cc3)

![alt](https://github.com/khoatna065/PBI_Inventory_Dashboard/assets/167158955/cf5de1af-3083-4c1b-aee7-217262c34edb)

![alt](https://github.com/khoatna065/PBI_Inventory_Dashboard/assets/167158955/f1f5962a-6ce9-4cd7-8433-b1359df1fc4e)

- ProductID, Product Name, Category, Subcategory (Dim_Category table)

![alt](https://github.com/khoatna065/PBI_Inventory_Dashboard/assets/167158955/96b389bd-4756-4b0f-9b42-4e0f4eb334bf)

![alt](https://github.com/khoatna065/PBI_Inventory_Dashboard/assets/167158955/98b795a6-2475-4ca9-8732-38ff5616a279)

## 2. Connect data to Power BI

- Connect queries above and available tables of dataset to PBI
- Modelling

![alt](https://github.com/khoatna065/PBI_Inventory_Dashboard/assets/167158955/9ee32224-4eef-4aa2-8977-8b9ffbdc606c)

## 3. Build dashboard

![alt](https://github.com/khoatna065/PBI_Inventory_Dashboard/assets/167158955/e31dea33-a14e-4b9d-bfde-647785462354)

![alt](https://github.com/khoatna065/PBI_Inventory_Dashboard/assets/167158955/c2a79222-5245-42b4-8284-e24c9960f2a2)


# III. Insight

1. Revenue - Inventory overview 
- Revenue tends to increase steadily from 2011 to the end of 2013. Every year, revenue usually peaks in the third quarter and gradually declines in the fourth quarter.
- Stock to sales ratio (average inventory value/sales) usually tends to decrease in the first quarter and increase in the following quarters. In 2014, this ratio increased significantly ⇒ Inventory efficiency is decreasing.
2. Revenue - Inventory by Category
- Revenue is only recorded from 2 categories: Bikes and Components
- The largest revenue come from the Bikes category at 140 million (88%), 7 times more than Components category.
- The Bikes category has the largest inventory value of 24,44M, nearly 4 times higher than the Components category (9M). The total stock value of other categories (Other, Clothing, Accessories) are not worth considering.
3. Revenue - Inventory by Sub-Category
- Top 3 Subcategory belong to Bikes category including Road Bikes, Mountain Bikes, and Touring Bikes, the rest belong to Components category.
4. Revenue - Inventory by Product
- Almost top sales products are belong to Bikes Category
5. Inventory by Location
- Locations that are occupying the highest amount of inventory are Subassembly (95K units) and Miscellaneous Storage (83K units), but have low total inventory values (3.3M and 1.5M respectively) => Store many items that are low-value
- Location Final Assembly, although not having a high inventory volume (20K, respectively), has the highest total inventory value (13.6M respectively) => Store items that are high-value.

# IV. Recommendation

- Adjusting the amount of inventory to increase or decrease in proportion to the rate of revenue fluctuations, with an increase in the third quarter of each year and a gradual decrease beginning in the fourth quarter.
- Research more about the reason the stock-to-sales ratio tends to rise in order to find solutions to lower inventory costs.
- Make a new marketing plan for Accessories, clothing, and Other categories because they are currently not bringing in revenue.
- Focus on promoting sales of HL Mountain Frame - Black, 38, HL Mountain Frame - Silver, 38 and Road-150 Red, 44 products, as well as products in Subcategory Wheels to resolve inventory backlog
- Notify and check with the production and purchasing departments about the products that are currently out of stock and adjust the Safety Stock level to suit the profitability of each product line.
- Many items are out of stock, so it is recommended to collect more opportunity cost data when an item is out of stock, which can be used to control and forecast future sales.
