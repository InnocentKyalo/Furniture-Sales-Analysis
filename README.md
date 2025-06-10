    Introduction
# 📊 Furniture Sales Inventory Analysis

This project analyzes a furniture inventory sales dataset downloaded from Kaggle. The dataset contains sales data with multiple columns, allowing for a multi-faceted exploration of patterns and trends in both **sales value** and **sales quantity**.

---

## 🎯 Objectives

1. **Breakdown Sales**  
   Understand how sales are distributed to help the marketing department identify areas to focus their efforts.

2. **Identify Sales Patterns**  
   Analyze trends over time by state, segment, and more to plan future strategies.

3. **Strategic Expansion**  
   Use historical sales data by region, category, and state to inform expansion plans.

4. **Order Fulfillment**  
   Investigate the order-to-ship duration to identify inefficiencies and improvement areas.

5. **Inventory Management**  
   Study inventory distribution and trends to optimize stock levels.

6. **Production Resource Allocation**  
   Identify high-demand products by segment to guide production investments.

7. **Risk Management**  
   Pinpoint low-demand periods by region or category to prevent overproduction.

8. **Market Segmentation**  
   Evaluate profitability by region, category, and customer group to identify high- and low-margin segments.

---

## ⚙️ Process

### 1. Data Profiling
- Dataset Size: **2,121 rows**, **21 columns**
- No missing values
- `RowID` column was not sequential

### 2. Data Cleaning
- `RowID`: Re-sequenced and formatted as whole number
- `Sales` & `Profit`: Formatted as decimals
- `Order Date` & `Ship Date`: Formatted as `dd-mm-yyyy`
- `Discount`: Converted to percentage format
- `Postal Code`: Formatted as whole number
- `Quantity`: Formatted as whole number

### 3. Data Transformation
- **Cost** = `Sales - Profit`
- **Unit Price** = `Sales ÷ Quantity`
- **Unit Cost** = `Cost ÷ Quantity`
- **Unit Profit** = `Profit ÷ Quantity`
- **Has_Discount**: Boolean column for discount presence
- **Order-Ship Duration**: Number of days between order and shipping
- **Profit Status**: Flag where `Unit Price < Unit Cost`
- **Date Table**: Created using `CALENDARAUTO()` in DAX  
  - Extracted: `Year`, `Month`, `Quarter` for time-based analysis

---

## 📁 Data Source

- [Kaggle Furniture Sales Dataset](https://www.kaggle.com/)  
  *(Provide direct dataset link if available)*

---

## 📌 Next Steps

- Visualize KPIs using Power BI (e.g., revenue by region, average shipping time)
- Explore predictive models to forecast demand
- Identify underperforming segments for strategic realignment


Data Modelling
-	Created date hierarchy with year, quarter, month, date
4.	Data Analysis
### Analysis Points

- **Revenue**
  - Total Sales  
  - Average Sales  
  - Total Cost  
  - Total Profit  
  - Sales per Region, Segment, Ship Mode, State, Period  

- **Inventory**
  - Total Units Sold  
  - Total SKUs  
  - Average Customer Quantity  
  - Inventory per Region, Segment, Ship Mode, State, Period  

- **Orders**
  - Total Orders  
  - Unique Orders  
  - Average Duration by Ship Mode  
  - Orders by Segment  
  - Order Trend Over Time  

- **Customers**
  - Total Customers  
  - Unique Customers  
  - Customer Discounts  
  - Sales per Region, Segment, Ship Mode,
. I wanted to understand the breakdown of sales both by value and quantity. There were multiple columns, and this presented an opportunity to analyze the data from several perspectives and identify patterns in the data.

Objectives
1.	Breakdown Sales. By understanding how their sales are broken down, the organization can understand their market better. This is key to the marketing department understanding where they might want to focus their efforts on.
2.	Identify Sales Patterns. Understanding the sales trends over the years by state, segmentation etc. to understand historical data and plan.
3.	Strategic Expansion. By understanding sales trends by state, category and region, management can make informed decisions on where to expand based on historical revenue.
4.	Order Fulfillment. Analyze the order to ship duration to understand which segments need improvement.
5.	Inventory. Understand inventory patterns, distribution
6.	Production Resource Allocation. To be efficient in production, the organization should understand the most in demand products by customer segmentation to understand where to invest more resources.
7.	Risk management. Analyzing which periods of the year demand is low for which state/ region/ category, management can plan to slow down production to avoid over-supply.
8.	Market Segmentation. Analyzing profitability of regions/ categories/ state/ cities, the organization can segment their market to know where the high & low margin customer categories lie.
Process
1.	Data Profiling
The dataset I used had 2121 rows and 21 columns. The dataset didn’t have any missing values therefore, it was easy to work with. The RowID column was not sequential.
2.	Data Cleaning
a)	Row-ID column had no sequential numbering – formatted the column to add sequential unique numbers & formatted as whole number.
b)	Sales & Profit columns formatted as decimal type for consistent data.
c)	Order & Ship date columns formatted as dd-mm-yyyy date format.
d)	Discount columns formatted as a percentage.
e)	Postal column formatted as whole number.
f)	Quantity column formatted as whole number.

3.	Data Transformation
   a.	Cost column addition. Sales less Profit.
   b.	Unit Price addition. Sales divided by Quantity.
   c.	Unit Cost addition. Total Cost divided by Quantity.
   d.	Unit Profit. Total Profit divided by quantity.
   e.	Has_Discount to identify orders with discounts.
   f.	Formatted Order Date and Ship Date to use a standard dd-mm-yyyy format.
   g.	Added Order-Ship Duration column to get number of days from ordering to shipping.
   h.	Added Profit_Status to show products that were sold at a lower Unit Price than Unit Cost
   i.	Added a Date table by using the CALENDARAUTO () DAX function to generate a list of dates from the data
-	Extracted year, month, quarter

Data Cleaning

Data Modelling
-	Created date hierarchy with year, quarter, month, date
  
4.	Data Analysis
The following were the analysis points:
-	Revenue
      o	Total Sales
      o	Average Sales
      o	Total Cost
      o	Total Profit
      o	Sales per Region, Segment, Ship Mode, State, Period, 
-	Inventory
      o	Total Units sold
      o	Total SKUs
      o	Average Customer Qty
      o	Inventory per Region, Segment, Ship Mode, State, Period

-	Orders
      o	Total Orders
      o	Unique Orders
      o	Average duration by ship mode
      o	Orders by segment
     o	Order trend over time
  
-	Customers
      o	Total Customers
      o	Unique Customers
      o	Customers discount
      o	Sales per Region, Segment, Ship Mode, State, Period, Sub-Category 
