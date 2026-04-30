# Does the Golden Cross REALLY Work? — Full Backtest

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/BacktestLAB/golden-cross-backtest/blob/main/golden_cross_backtest.ipynb)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **BacktestLAB — Video 8**  
> A scientific backtest of the Golden Cross strategy across 6 major assets, 20 years of daily data, with full parameter optimization and exit strategy comparison.

---

## 📺 Video

[![YouTube](https://img.shields.io/badge/YouTube-Watch%20Video-red?logo=youtube)](https://youtube.com/@BacktestLAB)

---

## 🗺️ What this notebook covers

| Section | Content |
|---------|---------|
| 1 | Setup — libraries, data loading from Yahoo Finance |
| 2 | Golden Cross on S&P 500 — Death Cross vs TP/SL 15%/5% exit |
| 3 | Multi-asset study — S&P 500, NASDAQ, AAPL, MSFT, NVDA, BTC |
| 4 | The bull market problem — why B&H always wins on trending assets |
| 5 | EUR/USD — a fairer test on a range-bound asset |
| 6 | TP/SL calibration — naive vs optimised exit parameters |
| 7 | MA optimisation — which window combination works best? |
| 8 | Scientific verdict — key findings and conclusions |

---

## 📊 Key Results

### Trending assets (10-year backtest)

| Asset | Strategy | Total Return | B&H Return | Alpha |
|-------|----------|-------------|------------|-------|
| S&P 500 | Death Cross | +93.7% | +190.6% | **-96.9%** |
| NASDAQ | Death Cross | +212.7% | +294.0% | **-81.3%** |
| AAPL | Death Cross | +240.5% | +752.5% | **-512%** |
| MSFT | Death Cross | +419.2% | +493.2% | **-74%** |
| NVDA | Death Cross | +6,475% | +6,652% | **-177%** |
| BTC | Death Cross | +8,033% | +10,452% | **-2,419%** |

**→ 12 / 12 strategies underperform Buy & Hold on trending assets.**

### Range-bound asset — EUR/USD (20-year backtest)

| MA Combo | Exit | Total Return | B&H Return | Sharpe |
|----------|------|-------------|------------|--------|
| 20/50 | Death Cross | +5.7% | -8.3% | 0.09 |
| **50/100** | **Death Cross** | **+22.9%** | **-9.8%** | **0.26** |
| 50/200 | Death Cross | -0.3% | -10.8% | 0.02 |
| 100/200 | Death Cross | -6.8% | -10.8% | -0.15 |

**→ MA 50/100 on EUR/USD beats Buy & Hold by +32.7 percentage points.**

---

## 🔬 The 3 Conditions for the Golden Cross to Work

```
1. The right asset    — range-bound, no strong secular trend
2. The right exit     — TP/SL calibrated to the asset's volatility
3. The right MA       — windows matched to the asset's cycle length
```

> *"The entry tells you when the trend starts.  
> The asset, the exit, and the parameters determine whether you profit from it."*

---

## 🚀 Quick Start

### Option 1 — Google Colab (recommended, no install needed)

Click the badge at the top of this README, or:

```
https://colab.research.google.com/github/BacktestLAB/golden-cross-backtest/blob/main/golden_cross_backtest.ipynb
```

### Option 2 — Run locally

```bash
# Clone the repo
git clone https://github.com/BacktestLAB/golden-cross-backtest.git
cd golden-cross-backtest

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook golden_cross_backtest.ipynb
```

---

## 📦 Dependencies

```
yfinance
pandas
numpy
plotly
jupyter
```

See `requirements.txt` for pinned versions.

---

## 📁 Repository Structure

```
golden-cross-backtest/
│
├── golden_cross_backtest.ipynb   ← Main notebook (run this)
├── requirements.txt              ← Python dependencies
├── README.md                     ← This file
└── LICENSE                       ← MIT License
```

---

## ⚠️ Disclaimer

This repository is for **educational purposes only**.  
Nothing here constitutes financial advice.  
Past backtest results do not guarantee future performance.

---

## 🔔 BacktestLAB

**Subscribe** for weekly scientific backtests — no hype, no guru content, just data and honest conclusions.

[![YouTube](https://img.shields.io/badge/YouTube-BacktestLAB-red?logo=youtube)](https://youtube.com/@BacktestLAB)

---

*MIT License — free to use, modify, and share with attribution.*
