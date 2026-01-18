# 📌 Project Title  
🛍️ Retail Product Performance Analysis  

# 📌 Introduction  
This project analyzes retail sales data to understand how different products contribute to revenue and overall business performance. Using Power BI, it identifies top revenue and volume drivers, classifies products as Value Drivers, Volume Drivers, or Supporting Products, and provides actionable insights by store, region, and sales channel.  

The analysis objectives include:
- Summarize product performance with total sales, quantity sold, and average selling price.  
- Identify high-value and high-volume products.  
- Classify products into Value, Volume, and Supporting categories.  
- Analyze performance across stores, regions, and channels.  
- Provide actionable business recommendations.

# 📂 Data Cleaning & Preparation

All datasets (sales and dimension tables) were imported into **Power BI** for cleaning and transformation.  
Several steps were carried out to ensure the data was accurate and analysis-ready.

---

### 🧹 Data Cleaning Overview

| Step | Description | Action Taken |
|------|-------------|--------------|
| Data Merging | Combined datasets | Merged all sales datasets into one table |
| Removed Duplicates | Eliminated duplicate records | Removed overall duplicates from the datasets |
| Checked for Blanks | Ensured data completeness | Checked for blanks in key columns |
| Data Type Validation | Ensured correct formats | Converted `order_datetime` to Date/Time and `order_date` to Date |
| Header Correction | Fixed column naming issues | Set the first row as headers in **Dim Regional Manager** table |

These steps ensured all datasets were clean, consistent, and ready for modeling and visualization in Power BI.

## ⚙️ CALCULATED FIELDS & MEASURES

To enable advanced time-based and performance analysis, calculated tables, columns, and measures were created in Power BI.

---

### 📅 Calculated Table

A dedicated **Date Table** was created to support time intelligence analysis.

**Table Name:** `DateTable`  
**Calculated Columns Created:**
- **Year** – Extracted year
- **Month** – Month name
- **MonthNumber** – Numeric month value (1–12)
- **Day of Week** – Day name (Monday–Sunday)
- **Day Number** – Numeric day value (1–31)

This table was linked to the sales table using `order_date`.

---

### 📊 Calculated Measures

#### 🔁 Growth & Comparison Measures

| Measure Name | Description |
|---------------|-------------|
| **%Revenue_Active** | Percentage of revenue from active products |
| **%ValueDriver_Revenue** | Share of revenue from value drivers |
| **%YoY_ASP** | Year-on-year change in ASP |
| **%YoY_Growth_Pct** | Year-on-year revenue growth |
| **%YoY_Quantity_Pct** | Year-on-year quantity growth |
| **ASP_LY** | Average Selling Price (Last Year) |
| **TotalSales_LY** | Total sales (Last Year) |
| **TotalQuantity_LY** | Total quantity sold (Last Year) |

---

#### 💰 Sales & Pricing Measures

| Measure Name | Description |
|---------------|-------------|
| **Total_Sales** | Total net sales revenue |
| **Average_Selling_Point** | Average selling price |
| **AvgSalesPerSubCategory** | Average sales by subcategory |
| **Revenue_Active** | Revenue from active products |
| **Revenue_Inactive** | Revenue from inactive products |
| **Revenue_Combo** | Combined revenue |
| **Supporting_Revenue** | Revenue from supporting products |
| **unit_price_ngn** | Unit price in NGN |

---

#### 📦 Volume & Quantity Measures

| Measure Name | Description |
|---------------|-------------|
| **Total_Quantity** | Total quantity sold |
| **QuantityRank** | Product ranking by quantity sold |
| **TopQuantityCount** | Count of top quantity products |

---

#### 🎯 Analysis & Driver Measures

| Measure Name | Description |
|---------------|-------------|
| **RevenueRank** | Product ranking by revenue |
| **TopRevenueCount** | Count of top revenue products |
| **ValueDriver_Revenue** | Revenue from value driver products |
| **VolumeDriver_Revenue** | Revenue from volume driver products |
| **SubCategoryClassification** | Product classification logic |
| **Top Region** | Best performing region |

These calculated fields enabled **product classification, performance ranking, growth analysis, and strategic insights** across regions, stores, and sales channels.

## 🔧 DATA TRANSFORMATION TOOLS USED

During the data preparation and transformation stage, the following tools were used to clean, format, and prepare the dataset for analysis:

| Tool / Platform | Purpose | Key Actions Performed |
|-----------------|---------|---------------------|
| **Power Query (Power BI)** | Data cleaning and transformation | Removed duplicates, checked for blanks, corrected data types, merged datasets |
| **DAX (Power BI)** | Advanced calculations | Created time intelligence measures, revenue metrics, ranking, and growth calculations |
| **Power BI** | Data visualization and analysis | Built interactive dashboards, KPIs, and performance charts |
| **GitHub** | Version control and documentation | Stored project files and documented analysis process |

---

These tools helped streamline **data ingestion, cleaning, transformation, analysis, and visualization** throughout the project lifecycle.

## 🔍 EXPLORATORY DATA ANALYSIS (EDA)

EDA was conducted to **understand patterns, distributions, and relationships** in the data before deeper analysis. The focus was on visual exploration and identifying areas of interest.

### 📊 Areas Explored

| Analysis Area | Focus |
|---------------|--------|
| Overall Business Performance | Evaluated total sales, total quantity sold, and ASP trends |
| Product Performance | Examined top and low-performing products by revenue and volume |
| Product Classification | Observed distribution across Value, Volume, and Supporting products |
| Order Type Analysis | Compared single items vs combos |
| Channel Performance | Visualized revenue contribution by Dine-in, Takeaway, Delivery, Drive-thru |
| Regional Distribution | Compared sales patterns across regions |
| Store Performance | Reviewed revenue and transactions by store |
| Time-Series Trends | Visualized monthly revenue and quantity trends |

EDA helped shape **dashboard design, KPI selection, and analytical focus**.

---

## 📊 STATISTICAL ANALYSIS

To complement EDA, **quantitative metrics and comparisons** were calculated to measure performance and growth more formally.

### 🔢 Methods Applied

| Method | Purpose |
|--------|---------|
| Percentage Change | Measured Year-on-Year (YoY) growth in revenue and quantity |
| Ranking Analysis | Ranked products, categories, and regions by revenue or quantity |
| Contribution Analysis | Calculated percentage of total revenue by product category or channel |
| Variance Analysis | Observed fluctuations in monthly sales and ASP |
| Time-Based Comparison | Compared current period vs previous period metrics (e.g., TotalSales_LY, TotalQuantity_LY) |

### 📐 Metrics Evaluated

- Year-on-Year Revenue Growth (%)  
- Year-on-Year Quantity Growth (%)  
- Average Selling Price (ASP) changes  
- Revenue contribution by product category, channel, and region  
- Monthly and seasonal performance variations  
- Top-performing products, regions, and stores by rank

This approach **quantified trends, measured performance, and supported actionable insights**, complementing the visual patterns observed during EDA.

---

## 📈 OVERALL PERFORMANCE

The business shows strong growth across revenue, volume, and market reach.

| Metric | Value | Notes |
|--------|-------|-------|
| **Total Sales** | ₦4.57B | Strong YoY growth; driven by volume increase |
| **Total Quantity Sold** | 2.51M units | Indicates higher product movement across stores |
| **Year-over-Year (YoY) Revenue Growth** | 63.20% | Substantial improvement from previous period |
| **YoY Quantity Growth** | 45.58% | Suggests volume sales are key growth driver |
| **Average Selling Price (ASP)** | Decreased by 11.19% | Indicates more promotions, discounts, or lower-priced items |
| **Top Performing Products** | Cake, Buckets | Consistently high in revenue and volume |
| **Order Type Distribution** | Singles: 73.12%, Combos: 26.88% | Singles dominate revenue share |
| **Primary Sales Channel** | Dine-in | Highest revenue and transaction volume |
| **Top Region** | North-East & North-West | Highest regional sales performance |
| **Star Store** | Store 11 | Leading store in revenue and transactions |

This high-level overview **sets the stage for deeper product, regional, and channel analysis** and provides context for KPIs and dashboards in the project.

## 💡 INSIGHTS & RECOMMENDATIONS

This section summarizes key findings from the **Product Performance Analysis** and provides actionable recommendations for management.

---

### 📊 High-Level Performance Metrics

| Metric | Value | Interpretation |
|--------|-------|----------------|
| **Total Sales** | ₦4.57B | 63.20% YoY growth indicates strong revenue increase |
| **Total Quantity Sold** | 2.51M units | 45.58% YoY increase shows growth is driven by volume |
| **Average Selling Price (ASP)** | Decreased by 11.19% | Suggests higher sales via discounts, cheaper bundles, or lower-priced items |

---

### 🛍️ Product & Category Insights

| Insight | Details |
|---------|---------|
| **Top Performers** | Cake and Buckets rank highest in both volume and revenue |
| **Order Type Distribution** | Singles dominate at 73.12% of revenue; Combos at 26.88% |
| **Revenue Drivers** | Supporting Products: ₦2.60B <br> Value Drivers: ₦1.18B <br> Volume Drivers: ₦785.12M |

---

### 🌍 Channel & Geographic Distribution

| Category | Details |
|----------|---------|
| **Primary Sales Channel** | Dine-in: ₦0.63B revenue, highest transactions (0.35M) |
| **Channel Trend** | Performance declines: Dine-in → Takeaway → Delivery → Drive-thru (lowest at ₦0.07B) |
| **Regional Performance** | Highest: North-East & North-West <br> Lowest: South-East & South-South |
| **Star Store** | Store 11 leads in revenue and transactions |

---

### 📅 Sales Trends & Seasonality

| Trend | Observation |
|-------|------------|
| **December Peak** | Highest sales: ₦156M, likely due to holiday demand |
| **Early Year Slump** | February lowest revenue (₦92M) and quantity |
| **Mid-Year Stability** | Stable revenue, slight downward trend June–November |
| **January Spike** | High quantity sold but not proportional revenue → possible promotions or discounts |

---

### 🎯 RECOMMENDATIONS

1. **Bundle of Stars Promotion** – Pair Buckets (family meal) with Cake (dessert) as a “Family Celebration Feast” to maximize top-performing products.  
2. **Review January Promotions** – Shift focus from low-margin Supporting Products to Value Drivers to increase profitability.  
3. **Upsell Initiative (Dine-in)** – Encourage customers buying high-volume singles to upgrade to Combos for marginal price increase.  
4. **Bucket Fest in Underperforming Regions** – Use Buckets as a promotional hook to drive penetration in South-East and South-South regions.

## MAINDASHBOARD
https://github.com/Ojoayobami/Retail-Product-Performance-Analysis/blob/main/Product%20Analysis%20-%20Dashboard%202.png?raw=true

<img width="1533" height="752" alt="image" src="https://github.com/user-attachments/assets/13fcb5dd-876e-4e08-823d-f001c544de0c" />

