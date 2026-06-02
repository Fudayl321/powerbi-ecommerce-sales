# E-Commerce Sales Performance

## Business Problem

[2-sentence description of the business problem this analysis solves and why it matters to the organisation.]

## Dataset

- **Source:** [Olist Brazilian E-Commerce — https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce]
- **Size:** [number of rows and columns]
- **Date range:** [YYYY to YYYY]

## Key Insights

- [Finding 1 with a specific number, e.g. "Revenue grew 23% YoY driven by Q4 peak demand"]
- [Finding 2 with a specific number]
- [Finding 3 with a specific number]
- [Finding 4 — optional]
- [Finding 5 — optional]

## Technical Stack

- **Tool:** Power BI Desktop
- **Data Prep:** [Python / SQL / Power Query — delete what doesn't apply]
- **Key DAX:** [List notable measures, e.g. CALCULATE, SAMEPERIODLASTYEAR, RANKX]
- **Features:** [e.g. Row-Level Security, Drillthrough pages, Bookmarks, Decomposition Tree]

## Screenshots

![Overview Dashboard](screenshots/overview.png)

## How to Run

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
2. Run `python python/prep.py` to clean and export to `data/cleaned.csv`
3. Open `report/report.pbix` in Power BI Desktop
4. In Power BI: Home → Transform Data → Data Source Settings → update path to `data/cleaned.csv`
5. Click Refresh
