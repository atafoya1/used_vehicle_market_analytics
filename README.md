# US Used Vehicle Market Dynamics & Pricing Variance (2014–2015)

An interactive, multi-tier Tableau portfolio dashboard analyzing **~558,000 used vehicle transactions** from the Kaggle Vehicle Sales and Market Trends dataset. This project explores macroeconomic trends, vehicle level valuation variances against MMR (Manheim Market Report) benchmarks, and granular brand pricing tiering.

## Live Interactive Dashboard
[🔗 View Live Interactive Dashboard on Tableau Public](https://public.tableau.com/views/USUsedVehicleMarketDynamicsPricingVariance/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## Dashboard Preview
<img width="953" height="574" alt="dashboard_preview" src="https://github.com/user-attachments/assets/145e8f12-cbeb-43c3-9997-4b1c275ff376" />

---

## Project Architecture & Analytical Narrative
The dashboard is structured into a cohesive 3-tier layout designed to guide viewers from high-level market macro trends down to granular asset-level insights:

1. **Macro Tier (Time Series Trends):** Tracks actual monthly average selling prices against market valuation benchmarks over time, revealing macro market shocks and recovery phases.
2. **Analytical Tier (Scatter Plot & Markups):** 
   * **Vehicle Level Valuation:** Compares individual actual sales prices against MMR benchmarks, utilizing dynamic conditional formatting (red/green tooltips) to isolate over- and under-priced units.
   * **Normalized Percentage Markup:** Analyzes relative pricing markups broken down hierarchically by manufacturer and body style.
3. **Brand Ranking & Variance Tier:** Evaluates nominal dollar price variances from brand benchmarks and ranks manufacturers by average selling price to isolate luxury vs. economy segments.

---

## Technical Stack & Data Engineering
* **Tool:** Tableau Desktop / Tableau Public
* **Data Source:** Kaggle Vehicle Sales and Market Trends Dataset (~558,000 rows)
* **Custom Calculations & Engineering:**
  * **`Clean State`:** Standardized raw state fields and filtered out CSV data alignment errors and text issues.
  * **Date Parsing:** Converted complex raw timezone strings into continuous analytical timelines.
  * **Dynamic Variance Tooltips:** Created calculated fields to drive mutually exclusive, conditional color coded variance indicators (`▲ Green` for above MMR, `▼ Red` for below MMR).
  * **Global Filtering:** Established cross sheet global filtering enabling dynamic multi region exploration.

---

## How to Explore
1. Click the Tableau Public link above to launch the interactive workbook.
2. Use the **States** filter sidebar to dynamically segment metrics by region.
3. Hover over data points on the scatter plot to inspect vehicle level price variances and dynamic benchmarks.
