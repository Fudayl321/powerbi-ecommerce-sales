# DAX Measures

Document every measure here as you build it. Include the purpose — this is what employers read.

---

## KPI Measures

### Total [Metric]
```dax
Total [Metric] = SUM('Table'[Column])
```
**Purpose:** Base measure — total value across all filters.

### [Metric] vs Target
```dax
[Metric] vs Target = DIVIDE([Total [Metric]], [Target], 0) - 1
```
**Purpose:** Percentage variance against target. Returns 0 (not BLANK) when target is missing.

---

## Time Intelligence

### YoY Growth %
```dax
YoY Growth % =
DIVIDE(
    [Total [Metric]] - CALCULATE([Total [Metric]], SAMEPERIODLASTYEAR('Date'[Date])),
    CALCULATE([Total [Metric]], SAMEPERIODLASTYEAR('Date'[Date]))
)
```
**Purpose:** Year-over-year percentage change. Requires a marked Date table.

### Rolling 3-Month Average
```dax
Rolling 3M Avg =
AVERAGEX(
    DATESINPERIOD('Date'[Date], LASTDATE('Date'[Date]), -3, MONTH),
    [Total [Metric]]
)
```
**Purpose:** Smooths short-term volatility to reveal trends.

---

## Ranking & Segmentation

### Top N Rank
```dax
Rank =
RANKX(ALL('Table'[Dimension]), [Total [Metric]], , DESC, DENSE)
```
**Purpose:** Dense rank — ties share the same rank, no gaps in sequence.
