# Lab 7: Planning and Learning Intergration

---

## Implemented Algorithms

- **Q-Learning (Baseline)** — model-free RL  
- **Dyna-Q** — integrates learning + model + planning  
  - Planning steps: `n ∈ {5, 10, 50}`  
- **Dyna-Q+** — adds exploration bonus for non-stationary environments  
- **Prioritized Sweeping** — planning using TD-error-based priority queue  

---

## Environment

- **Environment:** Taxi-v3  
- **State space:** 500 discrete states  
- **Action space:** 6 discrete actions  
- **Rewards:**
  - `-1` per step (efficiency penalty)
  - `-10` illegal actions
  - `+20` successful drop-off  
- **Episode ends:** successful drop-off or truncation  

---

## Key Features

- Tabular Q-learning using **NumPy arrays**
- Model learning via **Python dictionaries**
- Simulated planning updates
- Dynamic environment (reward modification after fixed steps)
- Exploration bonus:  R+ = R + κ√τ


Install dependencies:
 ```Python
 %pip install gymnasium numpy matplotlib
