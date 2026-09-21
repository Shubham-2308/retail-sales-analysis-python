# retail-sales-analysis-python
Exploratory analysis of 9,994 retail sales records using Python, Pandas, and Plotly to examine calendar-month sales patterns and product-category performance.
# Retail Sales Analysis with Python

Exploratory analysis of **9,994 retail sales line items** using **Python, Pandas, and Plotly** to examine calendar-month sales patterns and product-category performance.

## Business Scenario

A retail business wants to understand how sales vary across months and product categories.

This project investigates:

- Which calendar months contribute the highest and lowest combined sales?
- Which product categories generate the most sales?
- How is total sales distributed across categories?

The findings provide a starting point for further analysis of demand patterns and product performance.

## Project Overview

The analysis uses the **Sample Superstore dataset** and includes:

1. Inspecting data types, non-null counts, and descriptive statistics.
2. Converting order and shipping dates into datetime format.
3. Creating order-month, order-year, and day-of-week features.
4. Aggregating sales by calendar month and product category.
5. Creating interactive visualisations with Plotly.

## Dataset

The dataset contains **9,994 rows and 21 original columns**, including:

| Field | Description |
|---|---|
| Order ID | Order identifier |
| Order Date | Date the order was placed |
| Ship Date | Date the order was shipped |
| Segment | Existing customer segment |
| Category | Product category |
| Sub-Category | Product subcategory |
| Sales | Sales value per line item |
| Quantity | Units per line item |
| Discount | Recorded discount |
| Profit | Recorded profit |

**Each row represents a sales line item, not necessarily a unique order or customer.**

The CSV is not currently included in this repository.

## Tools and Technologies

- **Python** — Analysis workflow
- **Pandas** — Data inspection, transformation, and aggregation
- **Plotly Express** — Interactive charts
- **Jupyter Notebook** — Code and saved analysis outputs

## Key Findings

### Sales by Calendar Month

The analysis combines sales for each calendar month across all years in the dataset.

- **November** records the highest combined sales: approximately **352,461**.
- **February** records the lowest combined sales: approximately **59,751**.

These are combined calendar-month totals. They do not demonstrate year-over-year growth or establish that the same seasonal pattern occurs every year.

### Sales by Product Category

| Category | Total Sales |
|---|---:|
| Technology | 836,154.03 |
| Furniture | 741,999.80 |
| Office Supplies | 719,047.03 |

**Technology** contributes the highest sales value among the three categories.

Sales values are presented as recorded in the dataset. Higher sales do not necessarily mean higher profitability.

## Business Interpretation

The findings suggest several follow-up questions:

- Does the November sales peak occur consistently across individual years?
- Which subcategories contribute most to Technology sales?
- How do category profit margins compare?
- What relationship exists between discounts, sales, and profit?

These questions require additional analysis before making pricing, inventory, or investment recommendations.

## Repository Contents

- **E-Commerce project.ipynb** — Analysis notebook with code and saved outputs
- **README.md** — Project overview, findings, and setup instructions

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Shubham-2308/retail-sales-analysis-python.git
cd retail-sales-analysis-python
```

Alternatively, download and extract the repository ZIP file.

### 2. Install dependencies

```bash
pip install pandas numpy plotly notebook
```

### 3. Prepare the dataset

Obtain the **Sample Superstore CSV** used in the tutorial and place it in a folder named `data` inside the repository:

```text
retail-sales-analysis-python/
├── E-Commerce project.ipynb
├── README.md
└── data/
    └── Sample - Superstore.csv
```

The current notebook uses a local Windows file path. Before running it, replace the data-loading cell with:

```python
data = pd.read_csv(
    "data/Sample - Superstore.csv",
    encoding="latin-1"
)
```

### 4. Open the notebook

From the repository directory, run:

```bash
jupyter notebook
```

Open **E-Commerce project.ipynb**, restart the kernel, and run all cells in order.

**Note:** Interactive Plotly charts may not display fully in GitHub's notebook preview. Run the notebook locally to explore them.

## Limitations

- This is a learning project using sample retail data, not a live business deployment.
- Monthly sales are grouped by month number across all years.
- Analysis currently focuses on descriptive sales patterns and category comparisons.
- The notebook does not currently include forecasting, causal analysis, profitability modelling, or customer lifetime value.
- Data inspection covers data types and non-null counts; comprehensive duplicate and business-rule validation remains a planned improvement.

## Planned Improvements

- Add chronological year-month sales analysis.
- Use a bar chart for category comparisons.
- Calculate profit margins and examine discount patterns.
- Analyse distinct order counts and average order value.
- Explore order-to-shipment duration.
- Expand data-quality checks and written conclusions.
- Add chart images to the README.
- Replace the local dataset path with a relative path in the uploaded notebook.

## Learning Context and Attribution

This project was completed as a hands-on learning exercise following an online tutorial. It demonstrates my practice with data preparation, aggregation, and interactive visualisation.

**Tutorial:** [Watch the reference tutorial on YouTube](https://www.youtube.com/watch?v=cYKZltrlorQ)

The Sample Superstore dataset is used for educational analysis. I do not claim ownership of the dataset or tutorial material.

Author
Shubham Khairnar

[GitHub Profile](https://github.com/Shubham-2308)
