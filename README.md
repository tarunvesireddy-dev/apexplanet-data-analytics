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

with open('../README.md', 'a') as f:
    f.write(readme_addition)

print("README updated!")

print("README updated!")
