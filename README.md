# Dynamic Effect of Economic and Social Determinants on Nigerian Crime Rate: An Autoregressive Model with Exogenous and Interaction Terms

[![R](https://shields.io)](https://r-project.org)
[![Python](https://shields.io)](https://python.org)
[![License: MIT](https://shields.io)](https://opensource.org)

## Overview
This repository contains the reproducible **R** and **Python** scripts accompanying my MSc Statistics thesis at **Olabisi Onabanjo University (OOU), Ago-Iwoye, Ogun State, Nigeria (2026)**, supervised by **Dr. Taiwo I. Abass**.

The study investigates how macroeconomic shocks and socio-demographic determinants jointly influence crime dynamics in Nigeria. By combining autoregressive persistence with exogenous predictors and multiplicative interaction terms (**ARX**), the modeling pipeline quantifies both direct lagged effects and conditional interactions between economic and social variables.

---

## Repository Structure

```text
├── data/
│   ├── raw/                  # Raw macroeconomic, social, and crime datasets (or source metadata)
│   └── processed/            # Cleaned, stationarity-transformed time-series tables
├── r_scripts/
│   ├── 01_data_cleaning.R    # Missing value handling, log-transformations, and lag generation
│   ├── 02_unit_root_tests.R  # ADF, PP, and KPSS stationarity diagnostics
│   ├── 03_arx_estimation.R   # Dynamic ARX model estimation with interaction terms
│   └── 04_diagnostics.R      # Residual autocorrelation, heteroskedasticity, and stability tests
├── python_scripts/
│   ├── preprocessing.py      # Data pipeline and feature engineering (interaction & lag matrices)
│   ├── model_selection.py    # Information criteria (AIC/BIC) lag-length selection & forecasting
│   └── visualization.py      # Dynamic response plots and actual vs. fitted diagnostics
├── results/
│   ├── figures/              # Generated time-series and diagnostic figures
│   └── tables/               # Model parameter estimates and statistical test outputs
├── requirements.txt          # Python package dependencies
└── README.md
```

---

## Methodology Highlights
* **Dynamic Specification:** Models crime rate persistence via autoregressive lags ($Y_{t-p}$) alongside exogenous economic and social predictors ($X_{t-q}$).
* **Interaction Modeling:** Incorporates multiplicative interaction terms ($X_{1,t} \times X_{2,t}$) to evaluate how socio-demographic conditions amplify or mitigate macroeconomic stress.
* **Cross-Language Reproducibility:** Core preprocessing, lag optimization, and diagnostic checks are implemented across both **R** and **Python** for numerical verification.
* **Future Research Direction (Bayesian State-Space):** The modular pipeline provides a foundation for hierarchical Bayesian ARX and latent Gaussian spatio-temporal extensions (e.g., via `Stan` and `R-INLA`).

---

## Getting Started

### Prerequisites
* **R (≥ 4.3.0):** `tidyverse`, `forecast`, `tseries`, `lmtest`, `sandwich`, `dynlm`
* **Python (≥ 3.10):** `numpy`, `pandas`, `scipy`, `statsmodels`, `matplotlib`, `seaborn`

### Installation & Execution
1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd Dynamic-Effect-of-Economic-and-Social-Determinants-on-Nigerian-Crime-Rate
   ```

2. **Install Python dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the R estimation pipeline:**
   ```bash
   Rscript r_scripts/01_data_cleaning.R
   Rscript r_scripts/02_unit_root_tests.R
   Rscript r_scripts/03_arx_estimation.R
   Rscript r_scripts/04_diagnostics.R
   ```

4. **Run the Python verification & visualization scripts:**
   ```bash
   python python_scripts/preprocessing.py
   python python_scripts/model_selection.py
   python python_scripts/visualization.py
   ```

---

## Data Availability Note
Macroeconomic and social indicators were compiled from official releases by the **National Bureau of Statistics (NBS)** and the **Central Bank of Nigeria (CBN)**. Cleaned sample data is located in `data/processed/` to allow full end-to-end execution of all R and Python scripts.

---

## Citation
If you reference this codebase or methodology, please cite:
```bibtex
@mastersthesis{Nwani2026,
  author  = {Nwani, Ogonnaya},
  title   = {Dynamic Effect of Economic and Social Determinants on Nigerian Crime Rate: An Autoregressive Model with Exogenous and Interaction Terms},
  school  = {Olabisi Onabanjo University},
  address = {Ago-Iwoye, Ogun State, Nigeria},
  note    = {Supervisor: Dr. Taiwo I. Abass},
  year    = {2026}
}
```

## Contact
**Nwani Ogonnaya**  
MSc Statistics | BSc Computer Science with Statistics  
Department of Statistics, Olabisi Onabanjo University (OOU)  
GitHub: [://github.com](https://://github.com) | Email: [nwaniogonnayaabraham@gmail.com](mailto:nwaniogonnayaabraham@gmail.com)
