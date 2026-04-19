#  Deep Learning Time-Series Forecasting Benchmark

A comprehensive benchmarking system for **time-series forecasting** using multiple deep learning architectures including Dense, LSTM, GRU, CNN hybrids, Transformer, and xLSTM.

---

##  Project Overview

This project implements and compares **10+ deep learning models** for time-series forecasting.
The goal is to evaluate how different architectures perform on temporal data and identify the most effective model.

---

##  Models Implemented

###  Baseline Model

* Dense Neural Network (Non-sequence)

###  Sequence-Based Models

* LSTM
* GRU
* BiLSTM
* CNN-LSTM
* CNN-GRU
* CNN-BiLSTM
* Transformer
* CNN-Transformer
* xLSTM (Simplified)

---

##  Key Features

*  Fair evaluation framework for sequence models
*  Multiple performance metrics (MAE, MAPE, RMSE, R², etc.)
*  Residual analysis & correlation
*  Feature importance (gradients & weights)
*  Model saving & reproducibility
*  Prediction alignment for consistent comparison

---

##  Results Summary

###  Baseline Model

* **Dense Model**

  * MAE: **786**
  * MAPE: **2.5%**

>  Note: Dense model is not directly comparable with sequence models as it does not model temporal dependencies.

---

###  Sequence Models Ranking

| Rank | Model           | MAE    | MAPE  |
| ---- | --------------- | ------ | ----- |
|  1 | BiLSTM          | 1,416  | 3.9%  |
|  2 | CNN-LSTM        | 2,077  | 5.6%  |
|  3 | CNN-Transformer | 2,186  | 6.9%  |
| 4    | CNN-GRU         | 2,207  | 6.0%  |
| 5    | xLSTM           | 2,208  | 7.0%  |
| 6    | CNN-BiLSTM      | 2,586  | 7.7%  |
| 7    | LSTM            | 5,091  | 16.8% |
| 8    | Transformer     | 21,083 | 66.5% |

---

##  Key Insights

*  **BiLSTM performed best** among sequence models due to bidirectional context learning
*  **CNN-based hybrids improved performance** by extracting local temporal patterns
*  **Transformer underperformed** due to limited sequence length and dataset size
*  **xLSTM showed moderate performance** (simplified implementation)

---

##  Project Structure

```
├── models/
│   ├── dense_model.keras
│   ├── lstm_model.keras
│   ├── gru_model.keras
│   ├── transformer_model.keras
│
├── data/
│   ├── model_predictions.csv
│   ├── model_metrics.csv
│   ├── model_residuals.csv
│
├── scaler.pkl
├── notebook.ipynb
└── README.md
```

---

##  How to Run

```bash
# Clone repo
git clone https://github.com/your-username/time-series-forecasting-benchmark.git

# Install dependencies
pip install -r requirements.txt

# Run notebook or script
jupyter notebook
```

---

##  Outputs

*  Model metrics (`model_metrics.csv`)
*  Predictions (`model_predictions.csv`)
*  Residuals (`model_residuals.csv`)
*  Saved models (`.keras`)
*  Scaler (`scaler.pkl`)

---

##  Applications

* Energy demand forecasting
* Load prediction
* Time-series regression problems
* Real-time forecasting systems

---

##  Future Work

* Ensemble modeling (combine top models)
* Hyperparameter tuning
* Real-time deployment (API / dashboard)
* Attention optimization for Transformer

---

##  Author

**Rubab Qaiser**
BS Electronics | Deep Learning & Embedded Systems Enthusiast

---

##  Acknowledgment

This project demonstrates practical implementation and comparison of modern deep learning architectures for time-series forecasting.

---

##  License

This project is open-source and available under the MIT License.
