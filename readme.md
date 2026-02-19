# UPI Digital Payments Stress & Revenue Risk Model

Open this link Online - [![Open In Binder](https://mybinder.org/badge_logo.svg)](https://hub.gesis.mybinder.org/user/viknesh-data-up-ts-stress-model-dxvyg4rb/lab/workspaces/auto-a)

## Overview

This project analyzes the structural growth behavior of India's UPI ecosystem and models the financial impact of sustained transaction contraction scenarios.

The objective is to quantify:
- Deviation from expected growth trajectory
- Ecosystem value compression
- Bank-level revenue exposure
- Early warning triggers for systemic stress

The project uses publicly available NPCI monthly UPI statistics.

---

## Problem Statement

UPI has become India's primary digital payments infrastructure.  
While the system exhibits strong structural growth, sustained transaction contraction could materially impact:

- Merchant liquidity
- Digital commerce throughput
- Bank fee income
- Float-based earnings

This project answers:

> What happens if UPI transactions drop 5% month-over-month for multiple consecutive months?

---

## Dataset

Source: National Payments Corporation of India (NPCI)  
Period Covered: Mid-2022 to January 2026 (latest completed month)

Metrics used:
- Monthly Transaction Volume (Billion)
- Monthly Transaction Value (₹ Trillion)
- Average Ticket Size

---

## Methodology

### 1️⃣ Baseline Ecosystem Analysis
- Month-over-Month (MoM) Growth
- 3-Month Moving Average
- Historical Volatility (Standard Deviation)
- Volume CAGR
- Negative Month Frequency

### 2️⃣ Stress Scenario Modeling
Three contraction scenarios were simulated:

- Mild: -3% for 2 months
- Moderate: -5% for 3 months
- Severe: -7% for 6 months

Baseline projection assumes continuation of historical mean growth.

Metrics calculated:
- Volume deviation from baseline
- Relative deviation (%)
- Value impact (₹ Trillion)

### 3️⃣ Revenue Sensitivity Analysis
Assumptions:
- Bank market share: 12%
- Base fee realization: 0.10%
- 1 Trillion = 100,000 Crore

Revenue exposure calculated for each stress tier.

### 4️⃣ Statistical Context
Z-score classification used to measure extremity of contraction relative to historical volatility.

- Mild ≈ -1.25σ
- Moderate ≈ -1.66σ
- Severe ≈ -2.06σ

### 5️⃣ Early Warning Framework
Built a volatility-adjusted monitoring model:
- Watchlist trigger: Below Mean - 1σ
- Critical trigger: Below Mean - 2σ
- Consecutive contraction detection
- Automated revenue risk mapping

---

## Key Findings

- Mean Monthly Growth: ~3.2%
- Historical Volatility: ~4.95%
- Moderate stress causes ~22% deviation from expected trajectory
- Moderate scenario value impact: ~₹6.85 Trillion
- Bank-level exposure (12% share, 0.1% yield): ~₹82 Crore
- Sustained contraction produces structural deviation beyond normal cyclical volatility

---

## Business Implications

- Even statistically plausible contraction can materially impact transaction throughput.
- Revenue sensitivity is nonlinear when compounded across months.
- Early warning thresholds enable proactive monitoring rather than reactive reporting.
- Bank-level exposure depends heavily on effective yield realization.

This framework can be adapted to:
- Digital payment networks
- E-commerce GMV modeling
- Marketplace liquidity risk
- Fintech earnings sensitivity analysis

---

## Tools Used

- Python
- Pandas
- NumPy
- Jupyter Notebook

---

## Project Structure

UPI_Digital_Payments_Risk_Model/
│
├── Final_UPI_Analysis.ipynb ← Interview-ready version
├── notebooks/
│ └── UPI_EDA.ipynb ← Exploratory analysis
└── data/
└── cleaned_upi.csv

---

## Disclaimer

This analysis is for academic and portfolio purposes only.  
Revenue estimates are scenario-based approximations using simplified assumptions and do not represent actual bank financial disclosures.


---
