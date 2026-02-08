
# Multivariate Quality Control using PCA and Hotelling’s T²

## Overview
This project implements a **robust multivariate statistical process control (MSPC) pipeline** for monitoring complex, high-dimensional processes where quality depends on many correlated variables.

Traditional univariate control charts fail to detect multivariate drift and interaction effects.  
This notebook demonstrates how to **clean historical data (Phase I)** and **monitor new observations (Phase II)** using principled statistical methods.

The workflow reflects how multivariate quality monitoring is applied in **manufacturing, energy systems, and operational analytics**.

---

## Business Problem
In real-world processes, quality issues are costly when detected late.  
Modern systems generate dozens or hundreds of correlated measurements, making independent monitoring ineffective.

From a business perspective, delayed detection leads to:
- Increased scrap and rework
- Unplanned downtime
- Equipment degradation
- Compliance and reliability risk

The goal of this project is to **detect abnormal process behavior early**, using a statistically sound multivariate approach that reduces false alarms while capturing true process shifts.

---

## What This Project Does
This notebook builds an **end-to-end MSPC workflow**:

1. **Exploratory Data Analysis**
   - Understand variable distributions and potential anomalies
2. **Standardization**
   - Ensure scale-invariant modeling
3. **Dimensionality Reduction (PCA)**
   - Handle multicollinearity and stabilize covariance estimation
4. **Phase I: In-Control (IC) Identification**
   - Robust outlier detection using Elliptic Envelope
   - Validation with Mahalanobis distance and chi-square threshold
5. **Parameter Estimation**
   - Estimate mean vector and covariance matrix using IC data only
6. **Phase II: Monitoring**
   - Monitor new observations using Hotelling’s T² control chart
   - Flag deviations using statistically derived control limits

---

## Key Design Decisions
- **PCA before monitoring** to improve numerical stability and handle correlated variables
- **Robust Phase I cleaning** to avoid biased control limits from contaminated historical data
- **Hotelling’s T²** as a multivariate extension of traditional control charts
- **Statistical control limits** derived using F-distribution approximations

Each design choice is explicitly documented in the notebook using Markdown explanations.

---

## Outputs
The notebook produces:
- PCA scree plot (variance explained)
- PCA score plots for structural insight
- Phase I IC vs OOC classification
- Hotelling’s T² control chart for Phase II monitoring

These outputs support both **anomaly detection** and **process understanding**.

---

## Tech Stack
- **Python**
- NumPy, Pandas, SciPy
- scikit-learn (StandardScaler, PCA, EllipticEnvelope, EmpiricalCovariance)
- Matplotlib

---

## How to Run
1. Clone the repository
   ```bash
   git clone https://github.com/aksh-ay06/Quality-and-Reliability-Engineering-Final-Project
   cd /Quality-and-Reliability-Engineering-Final-Project
