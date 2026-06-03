# Enterprise Market Intelligence & Statistical Analytics Engine

A production-ready Python data pipeline designed to ingest real-time asset market data, execute rolling statistical modeling, and structure real-time analytics registries.

## 🛠️ Core Architecture & Engineering Features

* **Object-Oriented Pipeline:** Built using modular class structures (`MarketIntelligenceEngine`) ensuring scalable API routing and data state integrity.
* **Statistical Anomaly Detection:** Implements dynamically calculated Z-Scores based on rolling market variance and standard deviation to flag price fluctuations exceeding $|1.5|$ thresholds.
* **Data Efficiency Logic:** Computes volume-to-market-cap efficiency coefficients to gauge liquid velocity across continuous asset datasets.
* **Clean Data Engineering:** Leverages vectorized Pandas transformations for rapid execution without standard loops, bypassing typical bottlenecks.

## 💻 Technical Stack & Implementation

* **Language:** Python 3.x
* **Core Libraries:** Pandas, NumPy, Requests, IPython
* **Data Ingestion Vector:** Public REST API (No auth tokens required, engineered with timeout fault tolerance)

---

## 📊 Live Production Registry Output

When executed within the runtime pipeline, the engine analyzes live crypto/fiat vectors and structures the data stream into a dynamically styled analytics registry:

### 📈 Sample Dataset Snapshot (Live Ingestion Pipeline)

| # | Asset Name | Current Price | Market Cap | 24h Price Change | Price Z-Score | Volume/Mcap Efficiency |
|---|------------|---------------|------------|------------------|---------------|------------------------|
| 0 | Bitcoin    | $67,112.00    | $1,343,325,569,606| -2.63%           | -0.20         | 0.0214                 |
| 1 | Ethereum   | $1,873.96     | $225,941,882,057  | -5.15%           | -0.76         | 0.0381                 |
| 2 | Tether     | $1.00         | $187,852,449,039  | 0.01%            | 0.39          | 0.1450                 |
| 3 | BNB        | $635.56       | $85,481,263,368   | -5.87%           | -0.92         | 0.0112                 |
| 4 | Solana     | $75.10        | $43,409,181,346   | -4.72%           | -0.66         | 0.0543                 |

> *Note: The `price_z_score` metric actively identifies high-volatility anomalies. Assets flashing variations greater than $|1.5|$ are automatically routed into the statistical outlier processing thread.*

---

## 🚀 How To Run Locally

Clone the repository and install dependencies:
```bash
git clone [https://github.com/YOUR_GITHUB_USERNAME/market-intelligence-statistical-engine.git](https://github.com/YOUR_GITHUB_USERNAME/market-intelligence-statistical-engine.git)
pip install pandas requests numpy
python main.py
