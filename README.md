# 📊 Customer Behavior Data Analyst Portfolio Project

An end-to-end data analytics project focused on understanding customer purchasing behavior, subscription patterns, customer loyalty, and repeat purchases using **Python, SQL, PostgreSQL, and Power BI**.

This project demonstrates a practical data analytics workflow, from data cleaning and exploratory analysis to SQL-based business analysis and interactive dashboard development.

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Objectives](#-business-objectives)
- [Tools and Technologies](#-tools-and-technologies)
- [Project Workflow](#-project-workflow)
- [1. Data Preparation and EDA](#1-data-preparation-and-exploratory-data-analysis)
- [2. SQL Analysis](#2-sql-data-analysis)
- [3. Power BI Dashboard](#3-power-bi-dashboard)
- [Key Business Questions](#-key-business-questions)
- [Business Recommendations](#-business-recommendations)
- [Project Structure](#-project-structure)
- [How to Run the Project](#-how-to-run-the-project)
- [Key Learnings](#-key-learnings)
- [Future Improvements](#-future-improvements)
- [Acknowledgments](#-acknowledgments)
- [Author](#-author)

## 🎯 Project Overview

Understanding customer behavior is essential for businesses seeking to improve customer retention, optimize marketing campaigns, increase repeat purchases, and make better business decisions.

This project analyzes retail customer data to explore purchasing patterns, customer segments, subscription status, and repeat-purchase behavior.

The project follows a structured analytics workflow:

**Raw Data → Data Cleaning → Exploratory Data Analysis → SQL Analysis → Power BI Visualization → Business Insights**

The objective is to transform raw customer data into meaningful insights that can support data-driven business decisions.

## 🎯 Business Objectives

The major objectives of this project are:

- Analyze customer purchasing behavior and shopping patterns.
- Examine customer distribution across different subscription statuses.
- Investigate repeat-purchase behavior and customer loyalty.
- Identify patterns across customer demographics and purchase-related attributes.
- Use SQL to answer business questions through filtering, aggregation, grouping, and analytical queries.
- Develop an interactive Power BI dashboard to communicate findings.
- Translate analytical results into actionable business recommendations.

## 🛠️ Tools and Technologies

| Tool / Technology | Purpose |
|---|---|
| Python | Data preparation and exploratory data analysis |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Matplotlib / Seaborn | Exploratory data visualization, where used |
| PostgreSQL | Database storage and SQL-based analysis |
| SQL | Data querying, aggregation, and business analysis |
| Power BI Desktop | Interactive dashboards and visual reporting |
| Power Query | Data import and transformation |
| Git and GitHub | Version control and project documentation |

*The libraries and tools listed above should reflect the components actually used in this repository.*

## 🔄 Project Workflow

### 1. Data Collection and Understanding

The project begins with a retail customer dataset containing customer-related information and purchasing attributes.

The dataset is inspected to understand:

- The number of records and columns.
- Data types and column definitions.
- Missing or null values.
- Duplicate records.
- Potential inconsistencies and data quality issues.
- Variables relevant to customer behavior analysis.

### 2. Data Preparation and Exploratory Data Analysis

Python is used to inspect, clean, and prepare the dataset for further analysis.

### 3. Database Integration

The prepared data is loaded into PostgreSQL to support structured querying and business analysis.

### 4. SQL-Based Analysis

SQL queries are written to explore customer segments, subscription patterns, and purchase-related metrics.

### 5. Dashboard Development

Power BI is used to present analytical findings through visualizations and interactive reporting elements.

### 6. Interpretation and Recommendations

The findings are interpreted from a business perspective to identify potential opportunities for customer retention and improved purchasing behavior.

## 1. 🐍 Data Preparation and Exploratory Data Analysis

Python is used to understand the dataset, improve data quality, and prepare the data for analysis.

### Activities performed

- Imported the dataset into a Pandas DataFrame.
- Examined the dataset structure using methods such as `head()`, `info()`, and `describe()`.
- Checked for missing values and duplicate records.
- Reviewed data types and identified potential inconsistencies.
- Cleaned and transformed data where required.
- Explored customer characteristics and purchasing-related variables.
- Prepared the dataset for SQL analysis and dashboard development.

### Example Python operations

```python
import pandas as pd
import numpy as np

# Load the dataset
df = pd.read_csv("customer_shopping_behavior.csv")

# Inspect the data
print(df.head())
print(df.info())
print(df.describe())

# Check data quality
print(df.isnull().sum())
print(df.duplicated().sum())
```

*Replace the sample filename and code with the actual file and preprocessing steps used in your project.*

## 2. 🗄️ SQL Data Analysis

PostgreSQL is used to store and query the customer dataset. SQL helps answer business questions by filtering records, grouping customers, calculating metrics, and identifying relevant patterns.

### SQL concepts applied

Depending on the queries implemented in the repository, these concepts may include:

- `SELECT` and `DISTINCT`
- `WHERE` and `ORDER BY`
- Aggregate functions: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, and `MAX()`
- `GROUP BY` and `HAVING`
- Conditional logic using `CASE`
- Joins between related tables, where applicable
- Subqueries and Common Table Expressions (CTEs), where applicable
- Window functions such as `RANK()` and `DENSE_RANK()`, where applicable

### Example business query

**Question:** Which subscription statuses have at least five non-null previous-purchase records?

```sql
SELECT
    subscription_status,
    COUNT(previous_purchases) AS repeat_buyers
FROM customer
GROUP BY subscription_status
HAVING COUNT(previous_purchases) >= 5;
```

This query groups customers by subscription status and filters the resulting groups based on the number of non-null `previous_purchases` values.

**Important:** This example counts non-null values; it does not count individual customers who each made at least five purchases. The query should be adjusted if that is the intended business question.

### Example SQL analysis areas

- Customer distribution by subscription status.
- Average purchase-related metrics across customer segments.
- Repeat-purchase indicators.
- Customer comparisons across demographic or shopping attributes.
- Identification of customer groups that may benefit from targeted engagement.

The actual analysis should be documented alongside the SQL files included in this repository.

## 3. 📈 Power BI Dashboard

Power BI is used to transform analytical results into an interactive dashboard for easier interpretation.

### Dashboard objectives

- Present important customer behavior metrics in a clear format.
- Compare customer groups across relevant attributes.
- Highlight subscription and purchase-related patterns.
- Help users explore customer data through interactive visualizations.
- Support business discussions with accessible analytical summaries.

### Suggested visualizations

Include only the visualizations that are actually implemented in your dashboard.

- KPI cards for key customer metrics.
- Bar charts comparing customer groups.
- Donut charts showing subscription-status distribution.
- Column charts comparing purchase-related metrics.
- Slicers for relevant customer attributes.
- Tables displaying detailed analytical results.

### Dashboard Preview

Add a screenshot of your completed dashboard here.

```markdown
![Customer Behavior Power BI Dashboard](images/dashboard.png)
```

Replace `images/dashboard.png` with the actual path to your dashboard screenshot. If your repository does not contain an `images` folder, create one and upload the screenshot.

## ❓ Key Business Questions

This project is designed to investigate questions such as:

1. How are customers distributed across subscription statuses?
2. Which customer segments exhibit different purchasing patterns?
3. How does previous-purchase history vary across customer groups?
4. What customer characteristics are associated with repeat purchasing?
5. Which segments could be prioritized for retention campaigns?
6. How can customer behavior insights help improve marketing strategies?

These are analytical questions rather than confirmed findings. Answers should be added after examining the actual query outputs and dashboard results.

## 💡 Business Recommendations

The following are potential recommendations that should be validated against the analysis results before being presented as conclusions.

- **Customer retention:** Identify customer segments with lower engagement and evaluate targeted retention campaigns.
- **Subscription strategy:** Compare purchasing behavior across subscription statuses before designing subscription incentives.
- **Customer segmentation:** Group customers using relevant behavioral and demographic attributes to support targeted marketing.
- **Repeat-purchase growth:** Investigate the characteristics of frequent purchasers and test strategies that encourage additional purchases.
- **Data-driven decisions:** Use dashboard metrics to monitor changes in customer behavior and assess the impact of business initiatives.

## 📁 Project Structure

The repository may be organized as follows. Adjust the names to match your actual files and folders.

```text
Customer-Behavior-Data-Analyst-Portfolio/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── notebooks/
│   └── customer_behavior_analysis.ipynb
│
├── sql/
│   └── customer_behavior_analysis.sql
│
├── powerbi/
│   └── customer_behavior_dashboard.pbix
│
├── images/
│   └── dashboard.png
│
├── reports/
│   └── project_report.pdf
│
└── README.md
```

Do not include files or folders that are absent from your repository. If you use different filenames, update the structure accordingly.

## ⚙️ How to Run the Project

### Prerequisites

Install or set up the following tools as required:

- Python 3.x
- Jupyter Notebook or another Python environment
- PostgreSQL and pgAdmin
- Power BI Desktop
- Git (optional, for cloning the repository)

### Step 1: Clone the repository

```bash
git clone <your-github-repository-url>
cd <your-repository-folder>
```

Replace the placeholders with your actual GitHub repository URL and folder name.

### Step 2: Install Python dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Install only the libraries needed by your notebook.

### Step 3: Run the Python analysis

Open the notebook in Jupyter and execute its cells in order to inspect the dataset, perform preprocessing, and prepare the analysis data.

### Step 4: Set up PostgreSQL

1. Start your PostgreSQL server.
2. Create or select the database used by the project.
3. Import the prepared dataset into the appropriate table.
4. Open the SQL scripts in the `sql/` directory.
5. Execute the queries to reproduce the analysis.

Ensure that the database name, table name, column names, and PostgreSQL connection details match your actual setup.

### Step 5: Open the Power BI dashboard

1. Open the `.pbix` file using Power BI Desktop.
2. Configure the PostgreSQL data source if required.
3. Update the server, database, and authentication settings.
4. Refresh the dataset.
5. Review the visuals and interact with the available filters.

**Security note:** Never commit database passwords, API keys, or other credentials to GitHub. Use local configuration or environment variables for sensitive connection details.

## 📚 Key Learnings

This project provides practical exposure to:

- Data inspection, cleaning, and transformation using Python.
- Exploratory data analysis and interpretation.
- Relational database usage with PostgreSQL.
- SQL aggregation, grouping, filtering, and business-oriented queries.
- Connecting a database to Power BI.
- Building visual reports from structured data.
- Documenting an analytics workflow for reproducibility.
- Translating analytical questions into potential business actions.

## 🚀 Future Improvements

Potential improvements include:

- Adding more advanced customer segmentation.
- Developing customer retention and cohort analyses, if the dataset supports them.
- Creating reusable SQL views for recurring business metrics.
- Adding more interactive dashboard filters and drill-through pages.
- Automating data refresh and preprocessing.
- Adding a detailed data dictionary and reproducible environment configuration.
- Including validated findings, quantified recommendations, and a final project report.

## 🙌 Acknowledgments

This project was developed as a learning and portfolio exercise with reference to the existing Customer Behavior Data Analyst Portfolio Project by **Amlan Mohanty**.

The original project and associated tutorial helped guide the implementation workflow and the use of Python, SQL, and Power BI for customer behavior analysis.

Original project reference:

- **GitHub repository:** [Amlan Mohanty's Customer Behavior Data Analyst Portfolio Project](https://github.com/amlanmohanty/Customer-Behavior-Data-Analyst-Portfolio-Project)
- **YouTube tutorial:** [Watch the project tutorial](https://www.youtube.com/watch?v=5PrZvPeUw60)

Credit is provided to acknowledge the reference material. Any modifications, additional analyses, or original contributions should be described accurately in this repository.

## 👨‍💻 Author

**Arjun Pachori**

B.Tech Computer Science and Engineering — Artificial Intelligence and Machine Learning

**Areas of interest:** Data Analytics, Python, SQL, PostgreSQL, and Power BI.


---

⭐ If you find this project useful as a learning resource, feel free to explore the repository and its implementation.

*This repository is intended for educational and portfolio purposes. All findings and recommendations should be supported by the actual analysis results.*
