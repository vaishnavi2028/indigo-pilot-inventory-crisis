# Too Lean to Fly
Solving IndiGo’s Pilot Inventory Crisis Through Safety Stock and Service Level Optimization

**Management of Inventory Systems | Course Project - Spring Semester 2026 | Department of Industrial and Systems Engineering, IIT Kharagpur**  
Author: Sri Vaishnavi Viswanathan

---

## Files

| File | Description |
|------|-------------|
| `Management_of_Inventory_Systems_Course_Project - Case Study` | Case study report on optimizing Indigo's pilot safety stock and service level to prevent the 2025 operational crisis|
| `simulation_1_monte_carlo.py` | Monte Carlo validation of theoretical service levels |
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
SL  90.0%  |  N=2,337  |  Theoretical: 90.0%  |  Simulated: 89.97%  |  Δ = -0.03pp
SL  95.0%  |  N=2,410  |  Theoretical: 95.0%  |  Simulated: 95.11%  |  Δ = +0.11pp
SL  97.0%  |  N=2,455  |  Theoretical: 97.0%  |  Simulated: 97.03%  |  Δ = +0.03pp
SL  99.0%  |  N=2,544  |  Theoretical: 99.0%  |  Simulated: 99.02%  |  Δ = +0.02pp
SL  99.5%  |  N=2,593  |  Theoretical: 99.5%  |  Simulated: 99.51%  |  Δ = +0.01pp
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
