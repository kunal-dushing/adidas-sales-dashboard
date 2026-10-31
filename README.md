Adidas Sales Dashboard

An interactive sales analytics dashboard for a public Adidas US sales sample dataset covering 2020–2021.

**Live Demo:** [https://kd-adidas-sales-dashboard.vercel.app/](https://kd-adidas-sales-dashboard.vercel.app/)

## Features

- 9,648 source sales records summarized into 168 dashboard rows
- Interactive region and product filters
- KPI cards for reported sales, operating profit, units sold, and profit margin
- SVG charts for sales by region, profit contribution by region, sales by product, and yearly sales/profit
- Data-quality note explaining sales reconciliation and year-over-year limitations
- Responsive dark dashboard design

## Tech Stack

- Python and Pandas (data inspection, cleaning, grouping, and analysis in Google Colab)
- Vanilla HTML, CSS, and JavaScript (dashboard)
- Inline SVG (charts)
- GitHub (source control)
- Vercel (static hosting and GitHub-connected deploys)

## Data Analysis

1. Loaded the supplied Excel workbook in Google Colab with Pandas.
2. Inspected the 9,648 rows, field types, missing values, duplicates, and date range.
3. Grouped the data by year, region, product, and sales method to prepare dashboard summaries.
4. Preserved the source `Total Sales` and `Operating Profit` values in the dashboard.

### Data Quality Notes

- In 3,886 of 9,648 source rows, `Total Sales` is exactly 10 times `Price per Unit × Units Sold`.
- The dataset contains 1,302 rows for 2020 and 8,346 rows for 2021. Although both years cover all 12 months, the different row counts make year-over-year comparisons uncertain.
- This is a public sample dataset, not verified company-reported Adidas data.

## Local Development

No dependencies or build step are required. Open `index.html` in a modern browser.

To update the dashboard, edit `index.html`, commit the change to GitHub, and Vercel will deploy the connected repository.

## Project Structure

```text
adidas-sales-site/
├── index.html   # Dashboard, embedded summary data, filters, and charts
└── README.md    # Project overview, methodology, and live demo link
```

## Data Source

[Adidas US Sales Dataset on Kaggle](https://www.kaggle.com/datasets/heemalichaudhari/adidas-sales-dataset)
