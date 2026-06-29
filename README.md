# Too Lean to Fly
Solving IndiGo’s Pilot Inventory Crisis Through Safety Stock and Service Level Optimization

**Management of Inventory Systems | Course Project - Spring Semester 2026 | Department of Industrial and Systems Engineering, IIT Kharagpur**  
Author: Sri Vaishnavi Viswanathan

---

## Files

| File | Description |
|------|-------------|
| `Management_of_Inventory_Systems_Course_Project - Case Study` | Case study report on optimizing Indigo's pilot safety stock and service level to prevent the 2025 operational crisis|
| `simulation_1_monte_carlo.ipynb` | Monte Carlo validation of theoretical service levels |
| `simulation_1_monte_carlo.png` | Simulation Results Graph |

---

## Simulation - Monte Carlo Safety Stock Validation

Validates the theoretical service levels derived analytically in the case study by simulating monthly pilot demand from the fitted normal distribution and measuring empirical stockout frequency.

**Model:** `D ~ N(μ=2085, σ=197)` where σ combines absence, operational, and seasonal variability.

**What it does:**
- Runs 10,000 simulated months of pilot demand per service level
- Measures empirical stockout frequency and compares it to the theoretical target
- Plots the demand histogram with stockout zone highlighted
- Compares theoretical vs simulated service levels across all 5 candidates (90%, 95%, 97%, 99%, 99.5%)

**Output:** `simulation_1_monte_carlo.png`

```
python simulation_1_monte_carlo.py
```

Sample output:
```
SL  90.0%  |  N=2,337  |  Theoretical: 90.0%  |  Simulated: 90.05%  |  Δ = +0.05pp  |  Stockouts: 995
SL  95.0%  |  N=2,410  |  Theoretical: 95.0%  |  Simulated: 95.12%  |  Δ = +0.12pp  |  Stockouts: 488
SL  97.0%  |  N=2,455  |  Theoretical: 97.0%  |  Simulated: 96.95%  |  Δ = -0.05pp  |  Stockouts: 305
SL  99.0%  |  N=2,544  |  Theoretical: 99.0%  |  Simulated: 98.94%  |  Δ = -0.06pp  |  Stockouts: 106
SL  99.5%  |  N=2,593  |  Theoretical: 99.5%  |  Simulated: 99.48%  |  Δ = -0.02pp  |  Stockouts:  52
```

---

## Requirements

```
numpy
scipy
matplotlib
```

Install with:
```
pip install numpy scipy matplotlib
```

---

## References

See the full case study for references to IndiGo annual reports, FDTL regulatory documents, salary data, and aviation operations literature.
