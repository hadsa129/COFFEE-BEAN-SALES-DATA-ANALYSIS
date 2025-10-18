# ☕ Coffee Bean Sales Data Analysis

##  Project Overview
This project analyzes **coffee bean sales data** using **Microsoft Excel** to create an **interactive dashboard**.  
It demonstrates the complete data analysis workflow — from **data cleaning and transformation** to **visualization** and **reporting** — simulating real-world Data Analyst tasks.

---

##  Step 1: Data Overview
The dataset consists of three sheets:

| Sheet | Description |
|-------|------------|
| **Orders** | Order details: *Order ID*, *Order Date*, *Customer ID*, *Product ID*, *Quantity*. |
| **Customers** | Customer information: *Customer ID*, *Customer Name*, *Email*, *Phone Number*, *Address*, *City*, *Country*, *Postcode*, *Loyalty Card*. |
| **Products** | Coffee product info: *Product ID*, *Coffee Type*, *Roast Type*, *Size*, *Unit Price*, *Price per 100g*, *Profit*. |

---

##  Step 2: Data Gathering and Cleaning

Relevant columns from **Customers** and **Products** sheets were merged into the **Orders** table using:  
- **VLOOKUP** → to retrieve data from the Customers table  
- **INDEX + MATCH** → to retrieve data from the Products table  

###  Columns Added / Adjusted

| Column | Description / Formula |
|--------|----------------------|
| **Email** | Missing values replaced with blanks using `IF`. |
| **Sales** | Computed as `Quantity × Unit Price`. |
| **Coffee Type Name** | Nested `IF` to expand abbreviations: `Rob → Robusta`, `Exc → Excelsa`, `Ara → Arabica`, `Lib → Liberica`. |
| **Roast Type Name** | Expanded abbreviations: `M → Medium`, `L → Light`, `D → Dark`. |
| **Order Date** | Reformatted month as categorical to standardize across regions. |
| **Size** | Added unit "kg" to all entries. |
| **Unit Price & Sales** | Formatted as currency ($). |
| **Loyalty Card** | Created a column to indicate if a customer has a loyalty card. |

###  Additional Steps
- Checked and removed **duplicates**.  
- Converted the data range into an **Excel Table** named `Orders` for dynamic updates in Pivot Tables and Charts.

---

##  Step 3: Data Analysis & Visualization

### Pivot Tables and Charts

#### **1. Total Sales Sheet**
- Pivot Table `TotalSales` to visualize total sales by time period.  
- Grouped by **month and year** for detailed trend analysis.  
- Added **Coffee Type Name** (columns) and **Sales** (values).  
- Created a **2D Line Chart**.  
- Added **Timeline** for dynamic filtering.  
- Added **3 Slicers**: `Size`, `Roast Type Name`, `Loyalty Card`.

#### **2. Country Sales Chart**
- Bar chart ranking countries by total sales in descending order.

#### **3. Top 5 Customers**
- Bar chart showing only the top 5 customers by sales amount.

#### **4. Dashboard Sheet**
- Combined all charts into an **interactive Dashboard**.  
- Connected all **slicers and timeline** for unified dynamic filtering.

---

##  Key Learnings & Skills Demonstrated

| Category | Skills / Techniques |
|----------|-------------------|
| **Data Cleaning** | Handling missing values, formatting, duplicate detection |
| **Data Transformation** | VLOOKUP, INDEX/MATCH, nested IF, calculated columns |
| **Data Visualization** | Pivot Tables, Pivot Charts, Timelines, Slicers |
| **Dashboard Design** | Interactive filtering, chart linking, KPI visualization |
| **Excel Proficiency** | Dynamic tables, structured references, professional formatting |

---

##  Final Output
Interactive Excel Dashboard shows:  
- Monthly & yearly sales trends  
- Top-performing countries & customers  
- Coffee type performance by roast & size  
- Dynamic filters with Timeline & Slicers  

---

##  Conclusion
This project demonstrates Excel as a **powerful Data Analysis & Visualization tool**, from cleaning and merging multiple data sources to building an interactive business intelligence dashboard.
