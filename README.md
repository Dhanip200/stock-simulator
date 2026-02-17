# stock-simulator
📊 Monte Carlo Option Pricing Simulator

Make env and downlode requirements.txt
A Python-based Monte Carlo simulation framework for pricing European call and put options using Geometric Brownian Motion (GBM).

This project compares Monte Carlo estimated prices with the analytical Black-Scholes model and visualizes simulated stock paths through animation.

🚀 Project Overview

This simulator:

Generates stock price paths using Geometric Brownian Motion

Prices European options via Monte Carlo simulation

Computes analytical prices using the Black-Scholes formula

Compares numerical and theoretical results

Animates simulated stock price paths using Matplotlib

The goal is to demonstrate convergence of Monte Carlo pricing toward the Black-Scholes analytical solution as the number of simulations increases.

🧠 Financial Concepts Used

Geometric Brownian Motion

Risk-neutral valuation

Discounted expected payoff

Black-Scholes option pricing model

Numerical simulation & convergence

🛠 Technologies Used

Python

NumPy

Pandas

Matplotlib

SciPy

📂 Project Structure
├── monte_carlo_simulator.py
├── README.md

⚙️ Parameters

The simulation uses the following configurable parameters:

S0 = 100      # Initial stock price
K = 100       # Strike price
r = 0.05      # Risk-free rate
sigma = 0.2   # Volatility
T = 1.0       # Time to maturity (years)
steps = 252   # Time steps (daily)
n_paths = 1000

📈 How It Works
1️⃣ Stock Price Simulation

Stock prices follow the Geometric Brownian Motion model:

St=S0e(r−12σ2)t+σWt
S
t
	​

=S
0
	​

e
(r−
2
1
	​

σ
2
)t+σW
t
	​


Where:

r
r = risk-free rate

σ
σ = volatility

Wt
W
t
	​

 = Brownian motion

2️⃣ Monte Carlo Pricing

Simulate multiple stock price paths

Compute payoff at maturity

Take the average payoff

Discount to present value

Option Price=e−rTE[Payoff]
Option Price=e
−rT
E[Payoff]
3️⃣ Black-Scholes Formula

The analytical solution for European options is computed using:

C=S0N(d1)−Ke−rTN(d2)
C=S
0
	​

N(d
1
	​

)−Ke
−rT
N(d
2
	​

)
P=Ke−rTN(−d2)−S0N(−d1)
P=Ke
−rT
N(−d
2
	​

)−S
0
	​

N(−d
1
	​

)

This provides a benchmark to evaluate Monte Carlo accuracy.

🎥 Visualization

The simulator animates 20 sample stock paths to illustrate:

Random price evolution

Volatility impact

Distribution of terminal prices

Option prices and differences are displayed dynamically during animation.

📊 Sample Output
Option Price Comparison:

Method          Call Price   Put Price
Monte Carlo     10.43        5.57
Black-Scholes   10.45        5.58

Call Price Difference (MC - BS): -0.02
Put Price Difference (MC - BS): -0.01


Increasing n_paths reduces pricing error.

📌 Future Improvements

Variance reduction techniques (Antithetic variables, Control variates)

Stochastic volatility models (Heston)

Jump diffusion models (Merton)

Barrier or Asian option pricing

Performance optimization (vectorization / Numba)

🙏 Acknowledgment

This project was inspired and guided in part by resources available on GitHub https://github.com/tubakhxn/Monte-Carlo-Option-Pricing-Simulator/blob/main/README.md.
