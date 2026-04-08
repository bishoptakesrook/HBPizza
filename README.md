# 🍕 HB Pizza Analytics Project

## Overview

This project simulates a full-stack data analytics pipeline for a fictitious pizza and wings business, Hunt Advantage Group LLC. It showcases real-world data engineering practices using a medallion architecture (Bronze → Silver → Gold), Power BI reporting, and strategic orchestration under platform and licensing constraints. This project injects real world data chaos with the use of autogen python scripts causing correlations but not causations. It is an ongoing experiment to hone in on data wrangling skills.

The goal is to demonstrate technical depth, business storytelling, and adaptability in building scalable analytics solutions.

---
## Architecture

### 🥉 Bronze Layer – Raw Ingestion
- **Source**: Simulated CSV datasets with randomized rows and injected data quality issues
- **Files**:
  - `orders.csv`
  - `feedback.csv`
  - `inventory.csv`
  - `locations.csv`
  - `store_metrics.csv`

### 🥈 Silver Layer – Cleaned & Enriched
- **Tools**: Python (Pandas, TextBlob), Power Query (via Dataflow Gen1)
- **Transformations**:
  - Normalized column names and types
  - Cleaned nulls, fixed casing, trimmed strings
  - Calculated fields (e.g., `pizza_combo`, sentiment polarity)
  - Joined related datasets

### 🥇 Gold Layer – Modeled & Aggregated
- **Star Schema**:
  - `fact_orders`
  - `dim_store`
  - `dim_product`
  - `dim_date`
  - `fact_feedback`
  - `fact_metrics`
- **DAX Measures**:
  - `Total Sales`
  - `Average Order Value`
  - `Wings Mix`
  - `Avg Sentiment`

---

## Reporting

- **Tool**: Power BI Desktop
- **Report**: `Outreach.pbix`
- **Version Control**: `.pbit` templates stored in `/pbit_files/`
- **Visuals**:
  - Stacked columns for categorical comparisons.
  - Treemaps for Sales
  - Stacked bar for toppings count
  - Cluster column for date comparisons
  - Stacked columns for trend averages

---

## Platform Constraints & Workarounds

| Restriction | Workaround |
|------------|------------|
| Fabric trial provisioning expired | Pivoted to local medallion architecture using CSVs and Python |
| No OneDrive for Business | Used Power BI Desktop with local files and manual upload |
| Limited Dataflow Gen1 connectors | Published `.pbix` to activate workspace and unlock gateway |
| No Power BI Pro license | Used “Upload” feature in Power BI Service |
| Large `.pbix` files not Git-friendly | Used `.pbit` templates and changelog discipline |

---

---

## Related Projects

- [Academic DB Project — PostgreSQL ETL Pipeline](https://github.com/bishoptakesrook/scripting-databases)

---

## Author

**Jeremy Bishop**  
Entrepreneur — building interview-ready analytics solutions under 
real-world constraints.

---

<details>
<summary>📋 Project Wish List</summary>

<br>

**Cloud-to-Local Conversion Roadmap**  
*Avoiding free provisioning expirations while preserving the medallion architecture*

- [ ] **Forge the Local Database** — Use Python scripts to autogenerate 
  SQL DBA logic — not just for function, but for fun.
- [ ] **Extract the Bronze** — Generate CSVs from SQL views to serve as 
  raw data resources for local ingestion.
- [ ] **Refine the Silver** — Handle transformations in Power BI using 
  MQuery. Enhance time intelligence and prep for storytelling.
- [ ] **Wrangle the Chaos** — Apply EDA to uncover patterns, then flex 
  ExDA to document insights with clarity and impact.
- [ ] **Scout the Data Lake** — Research free or cost-effective cloud lake 
  options tailored for portfolio builders.
- [ ] **Rebuild the Cloud Castle** — Repeat the above processes in the 
  cloud once a sustainable, long-term platform is secured.

</details>

---

## Sharing & Access (Deprecated - Shown for past architecture mindset)

- **Fabric Workspace**: Bishappcore (access pending domain trust configuration)
- **Embedded Report**: Planned post-Gold layer finalization
- **Note**: This project is fictitious and intended for demonstration purposes only

---

## Repositories

- [GitHub – HB Pizza Analytics](https://github.com/bishoptakesrook/hbpizza)
- [Github - Academic DB Project](https://github.com/bishoptakesrook/scripting-databases)
---

## Author

**Jeremy Bishop**  
Entreprenuer 
Focused on building impactful, interview-ready analytics solutions under real-world constraints.

