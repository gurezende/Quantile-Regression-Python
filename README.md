# Quantile Regression vs. OLS: Prediction Intervals & Heteroscedasticity

A practical, hands-on repository demonstrating how to implement **Linear Quantile Regression** in Python using `statsmodels`. 

This code accompanies the article **"When OLS Fails: A Hands-On Guide to Quantile Regression and Prediction Intervals"** published on *Code Applied*.

![](coverquantile.jpeg)

## 📌 Overview

Ordinary Least Squares (OLS) regression models the **conditional mean** of a target variable. However, when data exhibits heteroscedasticity (non-constant variance) or heavy outliers, predicting the average alone can be misleading.

Quantile Regression allows you to:
- Predict any arbitrary percentile ($\tau$) of the target distribution.
- Capture asymmetric effects across features.
- Build dynamic, adaptive **90% prediction intervals** ($\tau = 0.05$ to $\tau = 0.95$).

## 🚀 Quick Start

### Prerequisites

Ensure you have Python 3.8+ installed along with the required dependencies:

```bash
pip install pandas numpy matplotlib statsmodels
```

### Running the Script

Clone the repository and run the main script to fit OLS and Quantile Regression models side-by-side:

```bash
python main.py
```

## 📊 Features & Output

1. **Synthetic Data Generation:** Creates a synthetic dataset featuring heteroscedastic noise (variance fans out as $X$ increases).
2. **Model Comparison:** Fits OLS alongside Quantile Regression models at $\tau = 0.05$, $\tau = 0.50$ (Median), and $\tau = 0.95$.
3. **Visualization:** Generates a publication-ready chart comparing the rigid OLS line against adaptive prediction bounds.
4. **Coefficient Summary Table:** Prints a side-by-side comparison showing how feature slopes shift across percentiles.

## 📈 Visualizing the Result

```
        / Upper Bound (P95)
       /  
======/===================  <-- Adaptive 90% Prediction Interval
     /
____/_____________________  <-- Lower Bound (P05)
```

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
