# Monte Carlo Risk Modelling - Learning Notes

Author: Parag Gupta

---

# 1. Purpose of the Project

The purpose of this project is to estimate financial risk using Monte Carlo simulation.

The workflow includes:

1. Defining portfolio parameters
2. Generating random market scenarios
3. Simulating future portfolio values
4. Estimating Value-at-Risk (VaR)
5. Visualising risk distributions

This type of analysis is commonly used in quantitative finance and risk management.

---

# 2. What is Monte Carlo Simulation?

Monte Carlo Simulation is a statistical technique that uses random sampling to model uncertainty.

Instead of predicting a single future outcome, the model generates many possible outcomes.

Examples:

- Stock prices
- Portfolio values
- Market risk
- Project uncertainty

The more simulations performed, the better the estimate of future behaviour.

---

# 3. Libraries Used

## NumPy

Import:

```python
import numpy as np
```

Purpose:

Used for:

- Random number generation
- Mathematical calculations
- Statistical operations
- Array processing

In this project NumPy generates random returns and computes portfolio paths.

---

## Pandas

Import:

```python
import pandas as pd
```

Purpose:

Provides structured data handling.

Although minimal in this project, Pandas is commonly used for financial datasets.

---

## Matplotlib

Import:

```python
import matplotlib.pyplot as plt
```

Purpose:

Used for visualising simulation results and portfolio distributions.

---

# 4. Portfolio Parameters

The simulation starts with:

Initial Investment

Example:

```text
£100,000
```

Expected Return

Example:

```text
8% per year
```

Volatility

Example:

```text
20% per year
```

Volatility measures uncertainty and risk.

Higher volatility generally implies higher risk.

---

# 5. What is Volatility?

Volatility measures how much asset prices fluctuate over time.

Low volatility:

- Stable prices

High volatility:

- Large price movements

Volatility is one of the most important variables in risk management.

---

# 6. Random Returns

Code:

```python
np.random.normal(...)
```

Purpose:

Generates random daily returns.

The simulation assumes returns follow a normal probability distribution.

Each simulation creates a different possible future market scenario.

---

# 7. Portfolio Simulation

Code:

```python
np.cumprod(...)
```

Purpose:

Calculates cumulative portfolio growth through time.

Each simulation produces a unique portfolio value trajectory.

Running many simulations provides a distribution of possible outcomes.

---

# 8. What is Stochastic Modelling?

A stochastic model contains randomness.

Unlike deterministic models, stochastic models acknowledge uncertainty.

Examples:

- Financial markets
- Weather systems
- Insurance claims
- Asset pricing

Monte Carlo simulation is a stochastic modelling technique.

---

# 9. Simulation Paths

Each line on the graph represents one possible future portfolio outcome.

Some paths perform well.

Some paths perform poorly.

Together they represent uncertainty in financial markets.

---

# 10. Value-at-Risk (VaR)

Definition:

Value-at-Risk estimates the maximum expected loss over a specified time period at a given confidence level.

Example:

95% VaR

Meaning:

There is a 95% probability that losses will not exceed the VaR value.

---

# 11. VaR Calculation

Code:

```python
np.percentile(...)
```

Purpose:

Finds the lower tail of the portfolio value distribution.

The 5th percentile is commonly used for 95% VaR calculations.

---

# 12. Interpretation of VaR

Example:

VaR = £15,000

Interpretation:

There is a 95% probability that losses will be less than £15,000 over the selected time horizon.

VaR does not predict the worst possible loss.

It estimates a confidence-based loss threshold.

---

# 13. Distribution Plot

Code:

```python
plt.hist(...)
```

Purpose:

Displays the distribution of final portfolio values.

The histogram shows:

- Most likely outcomes
- Extreme outcomes
- Portfolio risk spread

---

# 14. Applications

Monte Carlo methods are widely used in:

- Investment Banking
- Hedge Funds
- Asset Management
- Risk Management
- Insurance
- Derivatives Pricing

---

# 15. Overall Workflow

Portfolio Parameters
↓
Random Return Generation
↓
Monte Carlo Simulation
↓
Portfolio Value Paths
↓
Distribution Analysis
↓
Value-at-Risk Calculation
↓
Visualisation

---

# Interview Summary

If asked about the project:

"I developed a Monte Carlo simulation framework in Python to analyse portfolio risk. The project generated thousands of stochastic market scenarios using normally distributed returns and estimated Value-at-Risk (VaR) from the resulting distribution of portfolio outcomes. Through this work I strengthened my understanding of probability theory, stochastic modelling, risk management, and quantitative finance."
