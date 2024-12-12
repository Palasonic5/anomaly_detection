## Implementation for Anomaly Detection in Real-time Ad Performance Project

### Abstract
Anomaly detection is essential for monitoring and improving online advertisement performance. This project focuses on detecting anomalies in cost-per-click (CPC) and cost-per-thousand impressions (CPM) metrics using the realAdExchange dataset from the Numenta Anomaly Benchmark (NAB). We evaluated statistical models such as ARMA and Discrete Hidden Markov Models (dHMM) alongside machine learning techniques like LSTM networks, assessing their effectiveness through the NAB scoring framework. While ARMA and dHMM effectively captured normal patterns and transitions, LSTMs provided insights into sequential dependencies but struggled with limited data. This study underscores the importance of selecting appropriate models based on specific scenarios and contributes to advancing real-time anomaly detection for time-series data.

[Colab Link](https://colab.research.google.com/drive/1QQmDLQRASc2AhBTtHUKzMQerl_V987hq?usp=sharing)

### Results Preview

| Dataset | Model | TP  | FP  | FN  | TN   | NAB Score |
|---------|-------|------|------|------|------|-----------|
| CPC     | ARMA  | 2    | 4    | 163  | 1474 | 0.2923    |
|         | DHMM  | 2    | 1    | 163  | 1477 | **0.7064** |
|         | LSTM  | 0    | 0    | 165  | 1478 | -3.990    |
| CPM     | ARMA  | 3    | 3    | 161  | 1476 | **1.2747** |
|         | DHMM  | 3    | 11   | 161  | 1468 | 0.4747    |
|         | LSTM  | 0    | 0    | 164  | 1479 | -5.4299   |

