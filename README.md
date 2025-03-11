# 📈 Financial Options Pricing
## A Comparative Analysis between Classical Models and Machine Learning

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🎯 Research Focus

This study compares traditional pricing models with machine learning approaches to evaluate their effectiveness in predicting both theoretical and trading prices of financial options. A key focus is placed on the impact of historical volatility calculations across different time windows, demonstrating how these methodologies can complement each other in modern financial markets.

## 📊 Analysis Framework

### Pricing Methodologies
- 🔹 Black-Scholes Model
- 🔹 Monte Carlo Simulations
- 🔹 XGBoost (Machine Learning)

### Historical Volatility Windows
| Symbol | Time Period |
|--------|-------------|
| σ₁ | 1-year historical volatility |
| σ₂ | 2-year historical volatility |
| σ₃ | 3-year historical volatility |

### Price Types Analyzed
- 📊 Theoretical prices
- 💹 Trading prices


## 🔍 Key Findings

### Impact of Historical Volatility Windows

#### 📈 Call Options
- 1-year volatility (σ₁) provides optimal results for:
  - Black-Scholes (theoretical prices)
  - XGBoost (trading prices)

#### 📉 Put Options
- Monte Carlo shows best results with:
  - 3-year volatility (σ₃) for theoretical prices
  - 2-year volatility (σ₂) for trading prices

### 🎯 Model Performance
| Model | Best Performance |
|-------|-----------------|
| Black-Scholes | Theoretical Call prices |
| Monte Carlo | Put options pricing |
| XGBoost | Call options trading prices |

### 🔑 Critical Variables
- Historical volatility calculations
- Underlying bid/ask prices
- Greeks (trade vega and theta)

---

## **📦 Repository Structure**
```
Option_pricing_A_comparative_analysis/
├── 📂 FINAL_TRAIN_DATA_AND_ORIGINAL_DATASET/   # Data preprocessing & volatility computation
├── 📂 EXPLORATORY_ANALYSIS/                    # Initial statistical analysis
├── 📂 BLACK_SCHOLES/                           # Option pricing models
├── 📂 MONTECARLO/                              # Simulations and pricing
├── 📂 XGBOOST/                                 # Machine learning XGBoost models for option pricing
```

This structure provides a logical progression from raw data preparation to advanced modeling techniques. 🚀

```

### 📊 Dataset Contents
- Option prices (theoretical & trading)
- Underlying asset prices (bid/ask)
- Greeks (delta, gamma, vega, theta)
- Trading volumes and open interest
- Contract specifications
---
### Volatility Calculation Process (MAIN.R)


The script performs the following operations:

1.Extracts adjusted closing prices for each underlying asset


2.Calculates rolling historical volatility for three time windows:

-σ₁: (1 year)
-σ₂: (2 years)
-σ₃: (3 years)

with respect to the final transitions data


3.Merges volatility data with the original options dataset

---

## 🚀 Getting Started

1. Download `Option_pricing_A_comparative_analysis.zip`
2. Extract the contents
4. Review the analysis `/Thesis`

# Install required packages if not already installed
required_packages <- c(
  "xgboost",
  "Metrics",
  "doParallel",
  "dplyr",
  "caret",
  "ggplot2",
  "data.table",
  "tidyverse",
  "quantmod",
  "Rlof",
  "rpart",
  "knitr",
  "kableExtra",
  "gridExtra"
)

# Function to install missing packages
install_if_missing <- function(package) {
  if (!require(package, character.only = TRUE)) {
    install.packages(package)
    library(package, character.only = TRUE)
  }
}

# Install and load all required packages
invisible(sapply(required_packages, install_if_missing))

---
## 📈 Results 

- 📊 Model performance metrics
- 📉 Error distribution analysis
- 📈 Volatility impact studies
- 🔍 Market anomaly detection cases
- 📊 Comparative pricing charts

## 🤝 Contributing

We welcome contributions! Please feel free to submit a Pull Request.

## 📝 Citation

```bibtex
@article{options_pricing_analysis_2024,
    title={Variazioni della Volatilità Storica del sottostante ed il loro impatto sui modelli parametrici e non parametrici per il pricing delle opzioni: Un'Analisi Comparativa},
    author={[Giovanni Garofalo]},
    year={2024}
}
```

---
## 🏷️ Keywords

`#QuantitativeFinance` `#FinancialEngineering` `#MachineLearning` `#Options` `#Trading` `#DataScience` `#R` `#Quant`
