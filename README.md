Full time-series pipeline covering Sub-steps 1–5:

| Sub-step | Task | Status |
|----------|------|--------|
| 1 | E-commerce series: load, audit, clean, stationarity, decompose, ACF/PACF | Required |
| 2 | Sensor data: quality audit, fix duplicates/Inf/gaps/stuck sensors, label | Required |
| 3 | ARIMA baseline — order selection by AIC, temporal hold-out, MAE/RMSE/MAPE | Required |
| 4 | SARIMA + Prophet — seasonal models, comparison vs baseline | Required |
| 5 | GBM failure-risk classifier — 24h horizon, Recall-first, maintenance dashboard | Required |

## How to Run

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Place data files


### 3. Run the notebook

```bash
jupyter notebook week08_monday_timeseries.ipynb
```

Or execute non-interactively (for TA grading):
```bash
jupyter nbconvert --to notebook --execute week08_monday_timeseries.ipynb --output executed_output.ipynb
```

## Python Version & Packages

- **Python:** 3.10+
- **Key packages:** see `requirements.txt`

## Output Files

All plots are saved to `plots/`:


```
week-08/
└── monday/
    ├── week08_monday_timeseries.ipynb
    ├── README.md
    ├── ecommerce_sales_ts.csv      ← add from LMS (not committed)
    ├── sensor_data.csv             ← add from LMS (not committed)
    └── plots/
        └── *.png                   ← generated on run
```
