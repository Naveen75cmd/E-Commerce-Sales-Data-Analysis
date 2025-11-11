# E-commerce Sales Performance Dashboard

## Project Overview

This project involves the analysis of a transactional e-commerce dataset to uncover key business insights. The primary goal is to create a comprehensive, multi-page sales dashboard using Microsoft Power BI. The dashboard provides an at-a-glance view of sales performance, product trends, and customer behavior, enabling data-driven decision-making for marketing, sales, and inventory management.

The project is divided into two main phases:
1.  **Data Cleaning and Exploratory Data Analysis (EDA):** Performed in a Python environment (Google Colab/Jupyter Notebook) to prepare the data and uncover initial trends.
2.  **Dashboard Development:** The cleaned data is used to build an interactive and insightful dashboard in Power BI.

---

## Technologies Used

*   **Data Analysis:** Python
    *   **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
*   **BI & Visualization:** Microsoft Power BI
*   **IDE / Notebook:** Google Colaboratory / Jupyter Notebook
*   **Version Control:** Git & GitHub

---

## Features of the Dashboard

### Page 1: Sales Overview (Executive Summary)
*   **KPI Cards:** Total Sales, Total Profit, Total Orders, and Average Order Value.
*   **Visuals:**
    *   Sales and Profit trends over time (Area Chart).
    *   Sales contribution by product category (Donut Chart).
    *   Geographic sales performance by state (Map).
*   **Interactivity:** Slicers for filtering data by Year and Region.

### Page 2: Product Performance Analysis
*   **Visuals:**
    *   Top 10 best-selling products by Sales and Profit (Bar Charts).
    *   Detailed breakdown of Sales and Profit by Category and Sub-Category (Matrix Table with Conditional Formatting).
    *   Sales vs. Profit analysis to identify star performers (Scatter Plot).
*   **Interactivity:** Slicers for filtering by product Category.

### Page 3: Customer Analysis
*   **Visuals:**
    *   Top 10 customers by sales volume (Bar Chart).
    *   Sales distribution across customer segments (Column Chart).
    *   Geographic concentration of customers by city (Map).
    *   A detailed table view of customer metrics.
*   **Interactivity:** Slicers for filtering by customer Segment.

---

## How to Run This Project

### 1. Data Analysis (Python Notebook)

**Prerequisites:**
*   Python 3.x installed.
*   A virtual environment is recommended.

**Setup:**
1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name
    ```

2.  Create and activate a virtual environment (optional but recommended):
    ```bash
    # For Windows
    python -m venv venv
    .\venv\Scripts\activate

    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Notebook:**
    *   Open the `.ipynb` file in Jupyter Notebook or Google Colab.
    *   Place your raw dataset (e.g., `sales_data.csv`) in the root directory.
    *   Run the cells sequentially to perform data cleaning and analysis.
    *   The notebook will output a `cleaned_sales_data.csv` file, which will be used for the Power BI dashboard.

### 2. Power BI Dashboard

**Prerequisites:**
*   Microsoft Power BI Desktop installed.

**Setup:**
1.  Open the `Sales Dashboard.pbix` file included in this repository with Power BI Desktop.

2.  **Connecting to the Data Source:**
    *   If the dashboard shows an error regarding the data source, you will need to reconnect it.
    *   Go to **File > Options and settings > Data source settings**.
    *   Select the existing data source and click **Change Source**.
    *   Browse to the location of the `cleaned_sales_data.csv` file on your local machine and select it.
    *   Click **Apply Changes** when prompted.

3.  **Explore:** The dashboard is now fully interactive. Use the slicers and click on visuals to filter and explore the data.

---

## DAX Measures Used

Here are some of the key DAX measures created for the KPI cards and visuals:

*   **Total Sales:** `Total Sales = SUM('TableName'[Sales])`
*   **Total Profit:** `Total Profit = SUM('TableName'[Profit])`
*   **Total Orders:** `Total Orders = DISTINCTCOUNT('TableName'[Order ID])`
*   **Profit Margin:** `Profit Margin = DIVIDE([Total Profit], [Total Sales])`
*   **Average Order Value:** `Average Order Value = DIVIDE([Total Sales], [Total Orders])`

*(Note: 'TableName' should be replaced with the actual name of the data table in your Power BI model.)*
