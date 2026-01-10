Netflix Content & Member Insights Analysis

Role Alignment: Analytics Engineer – Member Insights Engineering

📌 Overview

This project analyzes Netflix’s global content catalog to understand how content composition, release timing, and geographic distribution shape member discovery and engagement. The analysis emphasizes analytics engineering principles—metric definition, data validation, and reusable insights—over one-off exploratory analysis.

🎯 Business Objective

Enable product, content, and engineering teams to:

Monitor catalog health

Improve content discovery

Inform global content investment decisions

📊 Key Questions

How has Netflix’s catalog evolved over time?

What is the balance between Movies and TV Shows?

Which countries and genres dominate the catalog?

How quickly does content become available after release?

Where do opportunities exist to improve discovery?

🧩 Data Source

Public Netflix Titles Dataset

~8,800 titles

Metadata includes content type, country, genre, rating, release year, and date added

This dataset mirrors the type of content metadata pipelines used in production analytics.

🛠 Analytics Engineering Approach
Data Cleaning & Validation

Normalized missing values (e.g., Unknown Director / Actor)

Standardized date fields into:

year_added

month_added

Validated null rates across key dimensions

Converted duration into numeric format for analysis

Feature Engineering

Content growth metrics

Content mix ratios

International content share

Release lag (release year → Netflix availability)

These features are designed to be materializable metrics suitable for dbt-style transformations.

📐 Metrics Defined
Metric	Description
Content Growth Rate	Titles added per year
Content Mix Ratio	Movies vs TV Shows
International Content Share	% non-US titles
Genre Concentration	Top genres as % of catalog
Release Lag	Years between release and Netflix availability
🔍 Key Insights

Sustained catalog growth with acceleration post-2016

Movies dominate volume, while TV Shows support longer-term engagement

Strong international expansion, led by the US, India, and the UK

Genre saturation in Dramas and Comedies

Short release lag supports timely discovery and engagement

💡 Business Impact

Discovery algorithms can benefit from greater genre diversification

International content remains a key growth lever

Monitoring release lag enables prioritization of ingestion pipelines

Metrics support experimentation, dashboards, and real-time monitoring

🧪 Tools & Technologies

Python (Pandas, NumPy)

Matplotlib, Seaborn

Jupyter Notebook
