# Sales Quantity Forecasting: Comparative Analysis (LSTM vs. Transformer vs. SARIMA)

## Research Motivation

The project began with the goal of improving sales forecasting using historical trends. While statistical models showed good performance, they struggled during sudden demand spikes caused by holidays and special events.

This led me to explore deep learning models such as LSTM and Transformers to better capture complex temporal patterns. The study ultimately focuses on building a forecasting system that is accurate, robust, and able to generalize to future demand variations.

## Project Overview

This project aims to forecast daily sales quantity using time series forecasting techniques. Traditional statistical models were first applied and showed good performance under normal conditions but struggled during sudden demand spikes such as holidays. To better capture complex patterns, deep learning models including Stacked LSTM and Transformer were implemented and compared. Among all models evaluated, the Stacked LSTM achieved the best predictive performance, demonstrating its effectiveness in modeling long-term dependencies and demand variability.

**Winner:** The **Stacked LSTM (Long Short-Term Memory) model** achieved the lowest prediction error, proving to be the most effective solution for this specific sales data.

## Research Objective

Real-world sales demand data often exhibit non-stationary behavior due to seasonality, external events, and sudden demand spikes during holidays and special occasions. These variations can violate the assumptions of traditional forecasting methods and lead to unstable predictive performance.

This project investigates how reliably time-series forecasting models perform under such changing conditions. Rather than focusing only on minimizing prediction error, the study explores the following question:

How reliably can forecasting models predict future demand when the data distribution shifts due to temporal changes and sudden demand spikes?

To address this, the project evaluates classical statistical models (ARIMA, SARIMA, Prophet) alongside deep learning approaches (Stacked LSTM and Transformer Encoder). The comparison considers predictive accuracy, model stability, and adaptability to demand fluctuations.

The broader goal is to move beyond accuracy alone and understand the robustness, generalization ability, and limitations of forecasting models in real-world environments.
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
