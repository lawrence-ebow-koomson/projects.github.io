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
