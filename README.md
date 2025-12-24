# 🛒 Retail Performance & Returns Analysis Dashboard

![Power BI](dashboard/MIS_Project(BI).pbix)

## 📖 Executive Summary

This project is a dynamic business intelligence solution designed to evaluate retail performance across multiple dimensions. Unlike standard sales dashboards, this tool places a heavy emphasis on **Year-over-Year (YoY) growth** and **Returns Analysis**, allowing stakeholders to not only see how much they sold, but also identify "friction points" where products are being returned by customers.

The dashboard integrates data from 2014 through 2017 (including order types and sales ledgers) to provide a single source of truth for decision-making.

---

## 📈 1. High-Level KPI Performance
The top section of the dashboard focuses on the "Pulse" of the business. It provides an immediate snapshot of health compared to the previous year for the selected timeframe.

### 🔹 Order Volume & Trends
**What this shows:**
This KPI card tracks the total number of orders placed in the selected year. It calculates the **Percentage Growth** compared to the previous year to measure market demand.
*   **Trend Analysis:** A monthly sparkline/chart visualizes seasonality, showing peak ordering months versus quiet periods.

![Orders KPI Screenshot](docs/orders_kpi.png)

### 🔹 Total Sales Revenue
**What this shows:**
A critical look at the top-line revenue. This section displays the total Dollar Value of sales for the selected year.
*   **Growth Metric:** It highlights the YoY revenue growth (or decline) percentage.
*   **Monthly Trend:** The trendline helps identify if revenue spikes align with marketing campaigns or holiday seasons.

![Sales KPI Screenshot](docs/sales_kpi.png)

### 🔹 Profitability & Margins
**What this shows:**
Revenue is vanity, profit is sanity. This KPI focuses on the actual bottom line after costs.
*   **Comparison:** It compares current year profit against the previous year.
*   **Trend:** The monthly trend reveals if the business is becoming more efficient or if margins are slipping during specific months.

![Profit KPI Screenshot](revenue_kpi.png)

---

## 📦 2. Product Sub-Category Performance

**Visual: Profit vs. Sales by Sub-Category**
**The Insight:**
This visualization answers the question: *"Are our high-volume products actually making money?"*
It plots Sub-Categories to see the relationship between how much we sell (Sales) and how much we make (Profit). This helps identify "Loss Leaders" (high sales, low/negative profit) versus "Star Products" (high sales, high profit).

![Sub-Category Comparison Screenshot](docs/revenue_by_sybcategory.png)
![Sub-Category Comparison Screenshot1](docs/sales_by_sybcategory.png)

---

## ↩️ 3. Returns & Quality Control Analysis
This section sets this dashboard apart by focusing on *Operational Efficiency*. High sales mean nothing if customers return the products.

### 🔹 Return Rate (Ratio) Analysis
**The Metric:** `(Total Returns / Total Orders)`
**The Insight:**
This looks at the *percentage* of orders that come back.
*   **YoY Growth:** Are customers returning items more frequently this year than last year?
*   **Monthly Comparison:** The chart compares the Return Rate of the current year vs. the previous year, month by month, to spot quality control issues or seasonal dissatisfaction.

![Return Rate Screenshot](docs/return_rate_kpi.png)

### 🔹 Return Volume (Count) Analysis
**The Metric:** Raw count of returned items.
**The Insight:**
While the *rate* is important, the *volume* impacts logistics. This visual tracks the exact number of returns.
*   **Trend:** Compares the raw number of returns this year vs. last year on a monthly basis, helping the warehouse team anticipate workload.

![Return Count Screenshot](docs/return_kpi.png)

### 🔹 Returns by Sub-Category
**The Insight:**
Which specific products are failing? This visual breaks down both the **Number of Returns** and the **Return Rate** by Sub-Category.
*   *Example:* If "Binders" have a low return rate but "Tables" have a high one, management knows to investigate the quality or shipping method for Tables.

![Sub-Category Returns Screenshot](return_by_subcategory)
![Sub-Category Returns Screenshot1](return_rate_by_subcategory)

---

## ⚙️ Interactivity & Dynamics

This dashboard is not a static PDF. It is built to be explored:

1.  **Yearly Selection:** The entire report changes based on the specific year selected, automatically recalculating "Previous Year" benchmarks.
2.  **Regional Filtering:** Users can drill down into specific regions (East, West, Central, South) to see if returns or sales issues are localized.
3.  **Category Filtering:** Isolate "Technology," "Furniture," or "Office Supplies" to see specific trends.

---

## 📂 Data Model & Technical Approach

The project utilizes a Star Schema approach in Power BI:
*   **Data Aggregation:** Merged historical files (`sale_2014`) with current ledgers (`sale_total`).
*   **Channel Segmentation:** Integrated `order type` data to distinguish between **Internet Sales** and **In-Shop** transactions.
*   **DAX Measures:** Extensive use of Time Intelligence functions (e.g., `SAMEPERIODLASTYEAR`, `CALCULATE`, `DIVIDE`) to generate dynamic YoY growth percentages.

---
*Created by [Your Name]*
