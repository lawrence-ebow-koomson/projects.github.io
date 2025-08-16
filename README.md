# Collateral Optimisation for Energy Trading

##  Overview
This project develops an optimisation framework to minimise collateral costs in energy trading while ensuring exposure coverage.  
The goal is to allocate different asset classes (cash, corporate bonds) efficiently across multiple counterparties, improving liquidity usage.

##  Methodology
- **Formulated as a Linear Programming (LP) problem** using `cvxpy`.
- Objective: minimise expected uncovered loss (EUL) subject to collateral and exposure constraints.
- Compared different allocation strategies:
  - **Pre-optimisation (baseline)**
  - **Greedy allocation**
  - **Convex optimisation with CVX**
- Evaluated results via allocation tables, expected uncovered loss, and visualisations.

##  Results
- Optimised allocation reduced **uncovered exposure** significantly across counterparties.
- Demonstrated efficient trade-offs between cash and corporate bond collateral.
- Produced comparative plots: baseline vs greedy vs CVX allocations.

## 🛠 Tech Stack
- Python (`cvxpy`, `numpy`, `pandas`, `matplotlib`, `seaborn`)
- Linear programming solver (`SCS`)

##  How to Run
```bash

# Install dependencies
pip install -r requirements.txt

# Run optimisation script
python collateral_optimisation.py
```


---



# Energy Price Risk & VaR Simulation

##  Overview
This project analyses daily energy price risk using **Value-at-Risk (VaR)** and **Expected Shortfall (CVaR)**.  
Monte Carlo simulation and bootstrapping techniques are applied to model portfolio risk under stressed conditions.

##  Methodology
- Collected synthetic daily price series for an energy portfolio.
- Computed **log returns** and distribution statistics.
- Applied **Monte Carlo Simulation** with 10,000+ trials to estimate portfolio VaR and CVaR.
- Bootstrapping approach for empirical VaR confidence intervals.
- Compared parametric, historical, and simulation-based risk measures.

##  Results
- Simulation-based VaR captured fat-tailed risk better than Gaussian parametric VaR.
- Bootstrapped confidence intervals validated stability of risk estimates.
- Visualised return distributions, simulated losses, and tail behaviour.

##  Tech Stack
- Python (`numpy`, `pandas`, `matplotlib`, `seaborn`)
- Risk analytics (`scipy.stats`)
- Simulation (`numpy.random`)

##  How to Run
```bash


# Install dependencies
pip install -r requirements.txt

# Run VaR simulation
python var_simulation.py
