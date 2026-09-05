## Key EDA Findings
- Dataset: 9,994 rows, 21 columns, no missing values
- Technology is most profitable category ($145K), Furniture least ($18K)
- Furniture has highest avg discount (17.4%) vs Technology (13.2%)
- Tables (-$17.7K) and Bookcases (-$3.5K) are net loss-making sub-categories
readme_addition = """

## Task 2: SQL for Data Extraction

**Objective:** Master SQL queries for data extraction and analysis using SQLite + Python integration.

### What was done
- Imported cleaned Superstore dataset into a SQLite database (`data/superstore.db`)
- Practiced SQL fundamentals: SELECT, WHERE, ORDER BY, LIMIT, GROUP BY, HAVING, JOIN
- Practiced advanced SQL: subqueries, CTEs (WITH clause), window functions (RANK, ROW_NUMBER, LAG), and views
- Connected Python to SQLite using SQLAlchemy
- Answered 10 business questions using SQL, including:
  - Top 5 products by sales
  - Monthly sales trend
  - Customer segmentation by spend
  - Most profitable region (**West**, ~$725K profit)
  - Loss-making orders by category
  - Top-selling sub-category per region
- Built a reusable database utility script (`scripts/db_utils.py`) with functions for connecting, querying, and summarizing data
- Saved all 10 queries to `scripts/queries.sql`

### Files
- `notebooks/t2_sql_extraction.ipynb` — full SQL practice + business question notebook
- `scripts/db_utils.py` — reusable database connection/query utilities
- `scripts/queries.sql` — all 10 business question queries
- `data/superstore.db` — SQLite database with the sales table
"""

with open('../README.md', 'a') as f:
    f.write(readme_addition)
    readme_addition = """

## Task 3: Data Visualization & Dashboarding

**Objective:** Create professional dashboards and visualizations.

### What was done

**Python Visualization**
- Created static plots using Matplotlib: line chart (monthly sales trend), bar chart (sales by category), scatter plot (discount vs profit), histogram (sales distribution)
- Created advanced plots using Seaborn: correlation heatmap, pairplot, boxplot (profit by category)
- Built interactive visualizations using Plotly (sales by region)
- Exported charts as PNG and HTML to the `reports/` folder

**Power BI Dashboard**
- Connected Power BI Desktop to the cleaned Superstore dataset
- Built an executive dashboard with:
  - KPI cards: Total Sales, Total Profit, Total Orders, Total Customers
  - Sales trend line chart
  - Category breakdown (bar/donut chart)
  - Geographic map by state/city
  - Top 10 products and customers
  - Filter panel with Region, Category, and Date slicers
- Created DAX measures, including Profit Margin %

### Files
- `notebooks/t3_visualization.ipynb` — Python visualization notebook (Matplotlib, Seaborn, Plotly)
- `reports/sales_by_category.png` — static chart export
- `reports/sales_by_region.html` — interactive chart export
- `dashboards/superstore_dashboard.pbix` — Power BI dashboard file

"""
readme_addition = """

## Task 4: Advanced Analytics & Statistical Modeling

**Objective:** Apply statistical analysis and basic predictive modeling.

### What was done

**Statistical Analysis**
- Computed descriptive statistics (mean, median, mode, std dev, skewness) for Sales, Profit, Discount, and Quantity
- Ran a t-test comparing profit between high-discount and low-discount orders
- Ran a chi-square test to check the relationship between Region and Category
- Calculated a 95% confidence interval for mean Profit

**Time Series Analysis**
- Converted Order Date into a time series index and resampled sales to monthly totals
- Decomposed monthly sales into trend, seasonality, and residual components
- Built a simple 3-month moving average forecast

**Customer Segmentation (K-Means Clustering)**
- Engineered RFM-style features (Total Sales, Total Profit, Order Count, Avg Discount) per customer
- Scaled features with StandardScaler and used the elbow method to select K=4
- Segmented customers into 4 clusters and visualized them with PCA (2D)
- Profiled and labeled each segment:
  - **VIP / Top Customers** — highest sales & profit, low discount → prioritize retention
  - **Loyal Frequent Buyers** — high order count, moderate discount → shift toward bundles over discounts
  - **Low-Engagement / Occasional Buyers** — low order count, low discount → re-engagement campaigns
  - **Discount-Sensitive / Unprofitable** — highest discount (25.6%), negative average profit → flag for discount policy review

**Predictive Model (Linear Regression)**
- Built a model to predict Profit from Sales, Quantity, Discount, Category, Sub-Category, and Region
- Results: R² = -0.64, MAE = $67.68, RMSE = $282.32
- Top influential features: Sub-Category (Copiers, positive), Discount (negative), Sub-Category (Machines, negative)
- The weak fit is attributed to extreme outlier orders; despite this, the model reinforces the project-wide finding that discounting is the strongest driver of reduced profit

### Files
- `notebooks/t4_advanced_analytics.ipynb` — statistical analysis, time series, clustering, and predictive modeling notebook
"""

with open('../README.md', 'a') as f:
    f.write(readme_addition)

print("README updated!")

with open('../README.md', 'a') as f:
    f.write(readme_addition)

print("README updated!")

print("README updated!")

readme_addition = """

## Task 5: Final Report, Automation & Presentation

**Objective:** Create final report, automate pipeline, and submit deliverables.

### What was done
- Created a 2-page executive summary PDF report with key findings, dashboard screenshot, and business recommendations
- Built an automated Python pipeline (`scripts/pipeline.py`) that loads raw data, cleans it, calculates KPIs, and exports to Excel
- Scheduled the pipeline to run automatically using Windows Task Scheduler
- Finalized repository with requirements.txt and complete documentation

### Files
- `reports/executive_summary.pdf` — final 2-page executive report
- `scripts/pipeline.py` — automated data pipeline
- `reports/pipeline_output.xlsx` — pipeline output (cleaned data + KPIs)
- `requirements.txt` — Python package dependencies
"""

with open('../README.md', 'a') as f:
    f.write(readme_addition)
print("README updated!")
