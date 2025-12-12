# Sales Quantity Forecasting: Comparative Analysis (LSTM vs. Transformer vs. SARIMA)

## Project Overview

This project implements and evaluates four distinct time series forecasting models—including advanced Deep Learning architectures—to predict daily sales quantity. The core objective was to **determine the most robust and accurate forecasting model** for optimizing inventory levels and strategic business planning.

**Winner:** The **Stacked LSTM (Long Short-Term Memory) model** achieved the lowest prediction error, proving to be the most effective solution for this specific sales data.

## Methodology and Models

The analysis rigorously compared four models on an unseen test set:

| Model Type | Model Name | Primary Mechanism |
| :--- | :--- | :--- |
| **Statistical** | SARIMA | Incorporates seasonal patterns into the ARIMA framework. |
| **Decomposition** | Prophet | Uses an additive/multiplicative model to handle trend and seasonality. |
| **Deep Learning (Recurrent)** | **Stacked LSTM (Winner)** | **Gated Memory Cells** to selectively remember information over long sequences. |
| **Deep Learning (Attention)** | Transformer Encoder | **Multi-Head Attention** to focus on the most relevant past data points. |

## 🏆 Key Results

The models were evaluated using industry-standard metrics, with **RMSE** (Root Mean Squared Error) as the primary focus, as it penalizes large forecasting errors.

| Model | RMSE | MAE |
| :--- | :--- | :--- |
| **LSTM** | **1074.41** | **332.24** |
| Transformer | [1084.72 ] | [410.23] |
| SARIMA | [1397.56] | [413.28] |
| Prophet | [1350.29] | [521.53] |

### Why LSTM Won:

The superior performance of the LSTM model is attributed to its **internal memory gates**, which excelled at capturing the complex, long-term dependencies and sequential flow within the sales data better than the other models.

## 🚀 Final Recommendation

The **LSTM Model** is the definitive recommendation for operational deployment due to its proven accuracy and low error rate.

* **Business Value:** This accuracy translates directly into **optimized inventory levels, minimized holding costs, and reduced risk of stock-outs.**

## 💡 Future Work

To evolve this project into a robust production system, future work should focus on:

1.  **Uncertainty Quantification:** Providing prediction intervals or confidence bounds around the forecasts for better risk management.
2.  **Exogenous Variables:** Incorporating external features like holidays, marketing spend, or competitor activities to further enhance accuracy.
3.  **Ensemble Modeling:** Exploring methods to combine the LSTM's strength with other models (like SARIMA) to potentially boost robustness.
