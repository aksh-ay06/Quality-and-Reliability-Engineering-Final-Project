# Multivariate Quality Control using PCA and Hotelling’s T²

## Overview
This repository contains a **course project for Quality and Reliability Engineering** that implements a **multivariate statistical process control (MSPC) pipeline** for monitoring high-dimensional, correlated process data.

Although developed in an academic setting, the project is structured to reflect **real-world quality and reliability engineering practices**, including robust baseline estimation and multivariate process monitoring.

---

## Course Context
- **Course:** Quality and Reliability Engineering  
- **Project Type:** Applied statistical analysis  
- **Focus:** Multivariate process monitoring and anomaly detection  

The objective was to design and implement a statistically sound approach for detecting abnormal process behavior in systems where quality depends on many interrelated variables.

---

## Business Problem (Applied Context)
In modern operational systems (manufacturing, energy, healthcare operations), quality issues are expensive when detected late.

Traditional univariate control charts monitor variables independently and fail to capture multivariate interactions, leading to delayed detection of process drift, increased scrap, rework, and operational risk.

This project addresses that gap by developing a **multivariate monitoring framework** that establishes a clean in-control baseline and detects deviations early.

---

## What This Project Does
The notebook implements an end-to-end **MSPC workflow**:

1. **Exploratory Data Analysis**
   - Assess distributions and potential anomalies
2. **Standardization**
   - Ensure scale-invariant analysis
3. **Dimensionality Reduction (PCA)**
   - Address multicollinearity and stabilize covariance estimation
4. **Phase I: In-Control (IC) Identification**
   - Robust outlier detection using Elliptic Envelope
   - Validation via Mahalanobis distance with chi-square thresholds
5. **Parameter Estimation**
   - Estimate mean vector and covariance matrix using IC data only
6. **Phase II: Monitoring**
   - Apply Hotelling’s T² control chart
   - Identify out-of-control observations using statistical control limits

---

## Key Design Decisions
- **PCA before monitoring** to handle correlated, high-dimensional variables
- **Robust Phase I cleaning** to avoid biased control limits
- **Hotelling’s T²** for multivariate monitoring
- **F-distribution–based control limits** for statistical validity

All design choices are documented directly in the notebook using Markdown explanations.

---

## Outputs
The notebook produces:
- PCA scree and score plots
- Phase I IC vs OOC classification
- Hotelling’s T² control chart for Phase II monitoring

These outputs support both anomaly detection and process understanding.

---

## Tech Stack
- **Python**
- NumPy, Pandas, SciPy
- scikit-learn
- Matplotlib

---

## Data
The dataset used in this project is not included.  
The analysis is **dataset-agnostic** and can be applied to any multivariate process data where rows represent observations and columns represent quality variables or sensor measurements.

---

## Why This Project Is Relevant Beyond the Classroom
This project demonstrates:
- Application of statistical quality control theory to realistic data
- Thoughtful methodological design, not black-box modeling
- Ability to reason about contamination, stability, and monitoring
- Clear communication of engineering decisions

---

## Possible Extensions
- Root-cause contribution analysis
- Adaptive control limits
- Real-time or streaming process monitoring
- Integration with dashboards or APIs

---

## Author
Akshay Patel  
Graduate Student – Industrial Engineering  


## How to Run
1. Clone the repository
   ```bash
   git clone https://github.com/aksh-ay06/Quality-and-Reliability-Engineering-Final-Project
   cd /Quality-and-Reliability-Engineering-Final-Project
