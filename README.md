# FTMUSDT 1-Minute Historical Kline Dataset

An institutional-grade, open-source archive of cleaned, standardized, and validated **1-minute intraday historical kline data** for **FTMUSDT** (Binance Spot).

---

## 📊 Dataset Specifications
- **Symbol:** `FTMUSDT`
- **Market:** Binance Spot
- **Timeframe:** 1 Minute (`1m`)
- **Total Months:** `68` months
- **Total Candles:** `2,938,791` 1-minute candles
- **Historical Range:** `2019-06-11 04:00:00` to `2025-01-13 02:59:00` (UTC)
- **Schema:** `timestamp, datetime_utc, open, high, low, close, volume, quote_volume, trade_count, taker_buy_volume, taker_buy_quote_volume`

---

## 🏛️ Directory Hierarchy
```text
FTMUSDT-Historical-Data/
├── README.md
└── 1m/
    └── <YYYY>/
        └── <MM>/
            └── FTMUSDT_1m_<YYYY-MM>.csv
```

---

## ⚡ 1-Line Pandas Stream Loader
Load any month directly from GitHub's raw CDN without cloning the repository:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/parshant231234-eng/FTMUSDT-Historical-Data/main/1m/2026/10/FTMUSDT_1m_2026-10.csv"
df = pd.read_csv(url)
print(df.head())
```
