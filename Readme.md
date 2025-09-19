# HFT Trading System

**An end-to-end pipeline for signal generation and strategy comparison (ML, Traditional, Deep Learning, RL).**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)]()

---

## Core Capabilities

- **Signal Pipeline**  
  - Download and preprocess real market data (Yahoo Finance).  
  - 59 engineered features: momentum, volatility, microstructure, volume.  
  - Unified input for ML and RL agents.  

- **Strategy Comparison**  
  - Machine Learning: Linear, Ridge, Random Forest.  
  - Traditional Quant: Momentum, Mean Reversion, Pairs Trading.  
  - Deep Learning: LSTM, GRU.  
  - Reinforcement Learning: PPO, SAC.  
  - Comprehensive metrics: Sharpe, Maximum Drawdown, Calmar, VaR, Information Coefficient.  

- **Fast & Research-Ready**  
  - Complete pipeline execution in under 2 seconds.  
  - Export results as CSV reports for further analysis.  

---

## Quick Start

```bash
git clone git@github.com:kevinlmf/HFT_System.git
cd HFT_System
pip install -r requirements.txt

# Run pipeline for signal generation
python run_complete_pipeline.py --symbol AAPL --quick

# Run full strategy comparison
python run_strategy_comparison.py --symbol AAPL --quick
```

Generated results are saved in the `exports/` directory.

---

## Example Results

```
Strategy                  Type         Ann.Ret   Sharpe   MaxDD   Assessment
ML - Linear               Machine Lea    8.6%     3.27     -0.5%   Best overall
ML - Ridge                Machine Lea    6.8%     2.54     -0.5%   Strong
LLM - LSTM                Deep Learni    3.1%     1.20     -0.2%   Moderate
Traditional - Momentum    Rule-based     1.9%    -0.05     -0.8%   Weak
```

---

## Project Structure

```
HFT_System/
├── run_complete_pipeline.py     # End-to-end signal pipeline
├── run_strategy_comparison.py   # Unified strategy comparison
├── data/                        # Data download and storage
├── signal_engine/               # Feature engineering and ML signals
├── strategy_methods/            # ML / Traditional / DL / RL implementations
├── evaluation/                  # Backtesting and performance metrics
├── exports/                     # Results (signals, metrics, reports)
└── README.md
```

---

## Documentation

For detailed explanations of features, metrics, and advanced usage, see  
[docs/README_full.md](docs/README_full.md).
