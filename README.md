# 🛒 Blinkit Grocery BI Dashboard Analysis

---

## 📑 Table of Contents

- <a href="#project-overview">📌 Project Overview</a>  
- <a href="#Project-context">🏢 Project Context</a>  
- <a href="#project-objectives">🎯 Project Objectives</a>  
- <a href="#target-audience">🔍 Target Audience</a>  
- <a href="#business-problems-addressed">🛑 Business Problems Addressed</a>  
- <a href="#key-features-&-visual-insights">💡 Key Features & Visual Insights</a>  
- <a href="#data-sources-&-description">📊 Data Sources & Description</a>  
- <a href="#project-lifecycle-&-technical-workflow">🔄 Project Lifecycle & Technical Workflow</a>  
- <a href="#data-modeling-approach">⚙️ Data Modeling Approach</a>  
- <a href="#dax-measures-implemented">🧮 DAX Measures Implemented</a>  
- <a href="#key-business-takeaways">📈 Key Business Takeaways</a>  
- <a href="#tools-&-technologies">📚 Tools & Technologies Used</a>  
- <a href="#conclusion">🔚 Conclusion</a>  
- <a href="#future-scope">🚀 Future Scope </a>  
- <a href="#how-to-use-this-project">📦 How to Use This Project</a>  
- <a href="#contact">📬 Connect with Me</a>  
- <a href="#dashboard-snapshot">🖼️ Dashboard Snapshot</a> 

---

## <span id="project-overview">🧩 Project Overview</span>  

This Power BI dashboard provides an in-depth analysis of BlinkIT’s grocery operations, highlighting trends in sales, customer ratings, and inventory performance across various outlet types, item categories, and geographic locations. The dashboard features dynamic KPI cards, DAX-driven metrics, and multiple chart types designed to uncover critical business patterns. It demonstrates how data visualization can convert raw operational data into actionable insights—supporting strategic expansion, customer satisfaction improvement, and performance optimization.

---

## <span id="project-context">🏢 Project Context</span>  

BlinkIT operates in a highly competitive grocery retail space, where understanding what sells, where it sells, and how customers respond is critical. However, the business lacked a centralized analytics solution to monitor these metrics in real-time. This Power BI project addresses the need for clarity in product performance, outlet analysis, and customer preferences by turning large-scale operational data into a user-friendly, interactive dashboard tailored for various stakeholders including marketing, operations, and analytics teams.

---

## <span id="project-objectives">🎯 Project Objectives</span>  

The main objective is to build a centralized business intelligence solution using Power BI to help stakeholders:

- Analyze sales performance by product type, fat content, and outlet size.
- Understand how inventory trends correlate with customer satisfaction.
- Compare regional performance using outlet location and establishment year.
- Present interactive KPIs such as Total Sales, Average Sales, and Ratings.
- Support data-driven decisions using clean, insightful visualizations.

---

## <span id="target-audience">🔍 Target Audience</span> 

- **Operations Managers** to monitor outlet efficiency and inventory flow.
- **Marketing Teams** to design campaigns targeting high-performing SKUs.
- **Sales Executives** to track regional and outlet-level performance.
- **Business Analysts** to identify patterns in customer behavior and stock trends.

---

## <span id="business-problems-addressed">🛑 Business Problems Addressed</span>

- ❌ No consolidated view of KPIs such as average sales or customer ratings.
- ❌ Lack of insight into how fat content affected item performance.
- ❌ Difficulty comparing outlet performance by type or physical size.
- ❌ No analytics to link inventory visibility with customer satisfaction.
- ❌ Absence of interactive, real-time dashboards for fast decisions.

---

## <span id="key-features-&-visual-insights">💡 Key Features & Visual Insights</span> 

### 1. KPI Cards

- 🟢 **Total Sales** – Overall revenue from all items sold.
- 🔵 **Average Sales** – Revenue per transaction or item.
- 🟡 **Number of Items Sold** – Total SKUs moved.
- 🔴 **Average Rating** – Customer satisfaction across product types.

### 2. Total Sales by Fat Content
A doughnut chart displays sales distribution between Regular and Low Fat items, showing a near 50-50 split.

### 3. Average Sales by Item Type
Dairy, Household, and Snack Foods outperform others; Baked Goods and Health items show lower engagement.

### 4. Sales by Fat Content & Outlet Type
Stacked column chart revealing consistent performance across outlet formats with slight regional preferences.

### 5. Sales by Outlet Establishment Year
Line chart showing post-2017 outlets contributing heavily to revenue.

### 6. Sales by Outlet Size
Tier 2 outlets lead sales with ₹369.28K, outperforming Tier 1 and Tier 3.

### 7. Sales by Outlet Location
Tier 2 outlets dominate sales; Tier 1 shows untapped potential.

### 8. All Metrics by Outlet Type

| Outlet Type         | Total Sales | Avg Sales | No. of Items | Avg Rating | Item Visibility |
|---------------------|-------------|-----------|--------------|------------|-----------------|
| Grocery Store       | ₹74,251.71  | 141.16    | 526          | 3.93       | 56.31           |
| Supermarket Type 1  | ₹739,886.89 | 139.92    | 5,235        | 3.92       | 338.65          |
| Supermarket Type 2  | ₹122,388.20 | 142.08    | 863          | 3.93       | 56.62           |
| **Total**           | ₹936,526.79 | 141.38    | 6,624        | 3.92       | 451.58          |

---

## <span id="data-sources-&-description">📊 Data Sources & Description</span> 

- **Sales Dataset** – Detailed transactions including item type, fat content, outlet size, sales value, ratings, and visibility.  
- **Outlet Dataset** – Information on outlet location, type, and establishment year.  
- **CSV Format** – Raw data imported from `.csv` files.  
- **Cleaned Data** – Post Power Query transformations ensuring accuracy and consistency.

---

## <span id="project-lifecycle-&-technical-workflow">🔄 Project Lifecycle & Technical Workflow</span> 

- **Requirement Gathering** – Understanding business goals and pain points.
- **Data Exploration** – Reviewing raw CSV files for sales and inventory.
- **Power BI Connection** – Importing and linking multiple datasets.
- **Data Cleaning** – Removing blanks, duplicates, and invalid entries.
- **Data Modeling** – Building relationships using a star schema.
- **Transformations** – Structuring data for analysis with Power Query.
- **DAX Measures** – Creating KPIs such as Total Sales, Avg Rating.
- **Dashboard Layout** – Designing a clean, filter-based UI.
- **Visual Development** – Implementing charts: bar, funnel, matrix, doughnut.
- **Insight Generation** – Identifying actionable business strategies.

---

## <span id="data-modeling-approach">⚙️ Data Modeling Approach</span> 

- **Schema** – Star Schema for optimized querying and relationships.  
- **Fact Table** – Sales data containing transactional measures.  
- **Dimension Tables** – Outlet, Item, and Location details.  
- **Relationships** – One-to-many and many-to-one relations based on IDs.

---

## <span id="dax-measures-implemented">🧮 DAX Measures Implemented</span> 


- **Total Sales** = `SUM(Sales)`  
- **Average Sales** = `DIVIDE(SUM(Sales), COUNTROWS(Sales))`  
- **Average Rating** = `AVERAGE(Rating)`  
- **Item Count** = `COUNT(Item_Identifier)`  
- **Sales by Fat Content** = Conditional SUM by category.

---

## <span id="key-business-takeaways">📈 Key Business Takeaways</span> 

- ✅ **Balanced Fat Content Demand** – Maintain variety in nutrition profiles.
- ✅ **Top Performers** – Dairy and snack items lead in revenue.
- ✅ **Modern Outlets Win** – Post-2017 outlets show higher sales velocity.
- ✅ **Tier 2 Locations** – Most profitable; ideal for expansion.
- ✅ **Supermarket Type 1** – Highest item visibility and revenue.
- ✅ **Shelf Visibility Impact** – Direct correlation with customer engagement.

---

## <span id="tools-&-technologies">📚 Tools & Technologies Used</span>

- **Power BI Desktop** – Report creation and publishing  
- **Power Query** – Data cleaning and transformation  
- **DAX (Data Analysis Expressions)** – Calculated fields and KPIs  
- **CSV / Excel** – Raw data sources  
- **Star Schema Modeling** – Relational structure

---
 
## <span id="conclusion">🔚 Conclusion</span>

The BlinkIT Power BI dashboard transforms siloed operational data into a centralized decision-support system. It empowers stakeholders to:

- Align inventory with customer preferences using rating insights  
- Expand in high-performing regions like Tier 2 cities  
- Promote top-selling items for profitability  
- Optimize outlet types and stocking plans

---

## <span id="future-scope">🚀 Future Scope</span>

- 🔮 Predictive analytics for sales forecasting  
- 🧮 Shelf-life and stock turnover insights  
- 🗺️ Geospatial outlet mapping and heatmaps  
- 👥 Customer segmentation and loyalty scoring  
- 📢 Campaign performance tracking

---

## <span id="how-to-use-this-project">📦 How to Use This Project</span>

1. **Download/Clone Repository**  
2. Open `.pbix` file in **Power BI Desktop**  
3. Connect your dataset or use sample data  
4. Explore visuals and interact with filters

---

## <span id="contact">📬 Connect with Me</span>  

<!-- Typing Animation / 🤝 Connect with me -->
[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=0DAD8D&lines=Let’s+connect+and+collaborate+on+meaningful+projects!;Click+the+buttons+below+to+connect+with+me+directly!)](https://git.io/typing-svg)

<div align="center">
<!-- 💼 LinkedIn -->
<a href="https://www.linkedin.com/in/rajeevtiwari8055"><img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn" width="30" height="30"/></a>
<!-- 📮 Gmail -->
<a href="mailto:rajeevtiwari8055@gmail.com" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/732/732200.png" alt="Email" width="35" height="35"></a>
<!-- ✖️ X -->
<a href="https://x.com/rajeevtiwariRT" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/5969/5969020.png" alt="X" width="35" height="35"></a>  
<!-- 🆔 GitHub -->
<a href="https://github.com/rajeevtiwari8055" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/733/733553.png" alt="GitHub" width="35" height="35"></a>
<!-- 🌐 Website -->
<a href="https://rajeevtiwari8055.github.io/" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/841/841364.png" alt="Website" width="35" height="35"></a>
</div>

<!-- Typing Animation / 🤝 Thanks for Visiting! -->
[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=8A2BE2&lines=🤝Thank+you+for+visiting+my+profile!)](https://git.io/typing-svg)

<!-- ⭐💫 Shower stars if you like my repos -->
<div align="center">
<img src="https://media.giphy.com/media/ObNTw8Uzwy6KQ/giphy.gif" width="30">
<a href="https://github.com/rajeevtiwari8055/rajeevtiwari8055" alt="GitHub Stars" title="Star my repositories">
<img src="https://img.shields.io/badge/Shower_stars_if_you_like_my_repositories-15k?style=for-the-badge&color=f9c513&logo=github&logoColor=black"/>
</a>
</div>

---

## <span id="dashboard-snapshot">🖼️ Dashboard Snapshot</span>

_Above: A sample view of the final dashboard showing KPIs, outlet-level charts, and product-level insights._

### 🖥️ Blinkit Dashboard View

![Blinkit Grocery Dashboard](BlinkIT%20Grocery%20Data.png)

### 🗂️ Project Preview Snapshot

![Blinkit Grocery Project Preview](BlinkIT%20Grocery%20Data1.png) 

---
