# Airbnb Analytics Dashboard Project

An interactive Business Intelligence solution developed in Power BI to analyze Airbnb listings, host performance, property pricing, and customer review trends across multiple major cities. This project transforms over 248,000 listings and 5.3 million reviews into actionable business intelligence.

## 📌 Project Overview
The dashboard converts raw, large-scale Airbnb data into meaningful trends using high-performance data cleaning pipelines, complex DAX calculations, and integrated Python script visualizations. 

It answers critical stakeholders questions regarding:
*   **Pricing trends** across different regions.
*   **Host performance** and metrics tracking Super Hosts.
*   **Customer satisfaction** and historical engagement.
*   **Property popularity** based on features and capacity.
*   **Revenue opportunities** derived from property optimizations.

---

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
| :--- | :--- |
| **Power BI** | Interactive dashboard development & report publishing. |
| **Python** | Data cleaning, outlier treatment, and advanced visual generations. |
| **Pandas** | Large-scale data manipulation and transformation. |
| **NumPy** | Numerical data and vector calculations. |
| **Power Query** | Core ETL processing and structural data modifications. |
| **DAX** | Custom calculated columns, business measures, and KPI logic. |
| **Matplotlib** | Statistical plotting integrated inside the analytics views. |

---

## 📊 Dataset Information
*   **Listings Dataset:** 248,000+ total entries containing 33 distinct features.
*   **Reviews Dataset:** 5.3 Million+ customer engagement logging rows.

### Data Cleaning Process (Jupyter Notebook)
1.  **Missing Value Treatment:** Handled null elements across `Bedrooms`, `Review Scores`, `Host Response Rate`, and `Host Acceptance Rate` via median imputation.
2.  **Duplicate Control:** Checked and permanently dropped duplicate data instances.
3.  **Type Conversions:** Cast object text columns `host_since` and `review_date` to native DateTime format.

---

## 🧠 Key DAX Measures Implemented
The project leverages custom Data Analysis Expressions (DAX) to drive interactive KPIs:

```dax
Accuracy Score = AVERAGE(Listings_Cleaned[review_scores_accuracy])
Average Price = AVERAGE(Listings_Cleaned[price])
Average Rating = AVERAGE(Listings_Cleaned[review_scores_rating])
Avg Acceptance Rate = AVERAGE(Listings_Cleaned[host_acceptance_rate])
Avg Accommodates = AVERAGE(Listings_Cleaned[accommodates])
Avg Bedrooms = AVERAGE(Listings_Cleaned[bedrooms])
Avg Listings per Host = DIVIDE([Total Listings], [Total Hosts])
Avg Response Rate = AVERAGE(Listings_Cleaned[host_response_rate])
Check-in Score = AVERAGE(Listings_Cleaned[review_scores_checkin])
Maximum Price = MAX(Listings_Cleaned[price])
Property Listings = COUNTROWS(Listings_Cleaned)
Total Hosts = DISTINCTCOUNT(Listings_Cleaned[host_id])
Total Listings = DISTINCTCOUNT(Listings_Cleaned[listing_id])
Total Reviews = COUNT(Reviews_Cleaned[review_id])
```

---

## 🖥️ Dashboard Architecture & Pages

### Page 1: Executive Summary
*   **Objective:** High-level overview of overall business volume and presence.
*   **Visual Elements:** KPI Cards, Listings by City, Room Type Distribution, Average Price by City, Top Property Types, Average Rating by Room Type.

### Page 2: Host Performance Analysis
*   **Objective:** Deep dive into host behavior, service speeds, and tier distributions.
*   **Visual Elements:** Super Host Distribution, Response Rate by City, Acceptance Rate by City, Top Hosts by Listings, Host Verification Analysis.

### Page 3: Property & Pricing Analysis
*   **Objective:** Break down price distributions and structural features.
*   **Visual Elements:** Average Price by City, Room Type Distribution, Instant Bookable Analysis, Property Type Analysis, Bedrooms vs. Price, Accommodates vs. Price.

### Page 4: Review Analytics
*   **Objective:** Track satisfaction baselines and customer growth over time.
*   **Visual Elements:** Average Rating by City, Average Rating by Room Type, Review Trend Analysis, Rating Distribution, Review Score Metrics.

### Page 5: Python Analytics & Advanced Insights
Advanced statistical graphs plotted via Python to uncover deep data correlations:
*   **Price Distribution Histogram:** Maps pricing clusters, concentrations, and structural outliers.
*   **Correlation Matrix Heatmap:** Checks mathematical dependencies between pricing, room size, accommodates, ratings, and location metrics.
*   **Property Type Box Plots:** Visualizes pricing variance across top 10 popular reservation configurations.

---

## 📈 Key Business Insights Generated
*   **Pricing Outliers:** Highly concentrated lower-to-middle tier values with prominent luxury outliers stretching the maximum range.
*   **Size vs. Revenue:** Strong mathematical correlations exist showing structural impacts on pricing based on bedroom capacity and accommodations volume.
*   **Host Efficiency:** Super Hosts display distinct response patterns and faster engagement loops across high-performing tourist hubs.

---

## 🚪 How to Open and Run the Dashboard
1. Ensure you have the latest version of [Power BI Desktop](https://microsoft.com) installed.
2. Ensure Python (`pandas`, `matplotlib`, and `seaborn`) is configured locally if you want to modify native Python visual steps.
3. Clone this repository to your desktop.
4. Open the `.pbix` dashboard file to explore live filters.

---

## Screenshots 

<img width="1366" height="768" alt="welcome" src="https://github.com/user-attachments/assets/d45748a6-2f06-4854-b754-2341fcee46f3" />

<img width="1366" height="768" alt="executive" src="https://github.com/user-attachments/assets/3bfd084c-d494-46b4-a789-500bb0f023f9" />

<img width="1366" height="768" alt="py analytics" src="https://github.com/user-attachments/assets/0b8c9327-c543-4491-9b66-bf2cbac41258" />
