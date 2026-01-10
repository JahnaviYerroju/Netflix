# Netflix Content & Member Insights Analysis

**Role Alignment:** Analytics Engineer – Member Insights Engineering

# Overview

This project analyzes Netflix’s global content catalog to understand how content composition, release timing, and geographic distribution influence member discovery and engagement. The analysis emphasizes analytics engineering principles such as metric definition, data validation, and reusable insights, rather than one-off exploratory analysis. The approach mirrors the type of content metadata pipelines used in production analytics.

# Business Objective

The goal of this analysis is to help Netflix’s product, content, and engineering teams:

- Monitor the health and evolution of the content catalog  
- Improve content discovery and recommendation strategies  
- Inform global content investment and acquisition decisions  

# Key Questions

- How has Netflix’s catalog evolved over time?  
- What is the balance between Movies and TV Shows?  
- Which countries and genres dominate the catalog?  
- How quickly does content become available after release?  
- Where are the opportunities to improve content discovery?  

# Data Source

- Dataset: Public Netflix Titles Dataset  
- Size: Approximately 8,800 titles  
- Metadata includes content type, country, genre, rating, release year, and date added  
- The dataset mirrors production-level content metadata pipelines  

# Analytics Engineering Approach

## Data Cleaning and Validation

- Normalized missing values (e.g., Unknown Director or Actor)  
- Standardized date fields into `year_added` and `month_added`  
- Validated null rates across key dimensions  
- Converted duration fields into numeric format  

## Feature Engineering

- Content growth metrics (titles added per year)  
- Content mix ratios (Movies vs TV Shows)  
- International content share (% non-US titles)  
- Release lag (years between release and Netflix availability)  

These features are designed as materializable metrics suitable for dbt-style transformations and reusable in dashboards or analytics pipelines.

# Metrics Defined

| Metric | Description |
|--------|------------|
| Content Growth Rate | Titles added per year |
| Content Mix Ratio | Ratio of Movies vs TV Shows |
| International Content Share | Percentage of non-US titles |
| Genre Concentration | Top genres as a share of the catalog |
| Release Lag | Years between original release and Netflix availability |

# Key Insights

- Sustained catalog growth with acceleration post-2016  
- Movies dominate in volume, while TV Shows drive longer-term engagement  
- Strong international expansion led by the US, India, and the UK  
- Genre saturation in Dramas and Comedies  
- Short release lag supports timely discovery and engagement  

# Business Impact

- Content discovery algorithms could benefit from greater genre diversification  
- International content remains a key growth lever  
- Monitoring release lag helps prioritize ingestion pipelines  
- Defined metrics support experimentation, dashboards, and real-time monitoring  

# Tools and Technologies

- Python: Pandas, NumPy  
- Visualization: Matplotlib, Seaborn  
- Environment: Jupyter Notebook
