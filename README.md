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

- [Kaggle Furniture Sales Dataset](https://www.kaggle.com/datasets/zahraaalaatageldein/sales-for-furniture-store)  
 
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
  - Sales per Region, Segment, Ship Mode

  Report Pages
  1. **Revenue**
  <img width="1306" height="725" alt="Revenue" src="https://github.com/user-attachments/assets/42e7da68-28a3-44ba-a8b7-278abeea1e57" />

  2. **Inventory**
  <img width="1290" height="731" alt="image" src="https://github.com/user-attachments/assets/dbc3b370-3e89-4688-a7f2-254ea7185be8" />

  3. **Customers**
  <img width="1299" height="732" alt="image" src="https://github.com/user-attachments/assets/6f6aa754-b1e5-49fd-91f2-4ebb3694893f" />

  4. **Orders**
  <img width="2398" height="1334" alt="image" src="https://github.com/user-attachments/assets/875541d1-e9a0-4b02-b5d9-435dd53e46b0" />

     




