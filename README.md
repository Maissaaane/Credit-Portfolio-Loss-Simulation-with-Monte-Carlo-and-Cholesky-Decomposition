# Credit-Portfolio-Loss-Simulation-with-Monte-Carlo-and-Cholesky-Decomposition

This project presents a quantitative analysis and simulation of credit risk for a portfolio of three distinct corporate entities. It uses a Monte Carlo simulation to build a probability density distribution of total losses and to calculate key risk metrics.

# Key Features
Correlated Default Simulation: Uses a Cholesky decomposition of a correlation matrix to simulate correlated default events for three different company categories.

Loss Distribution Analysis: Performs 10,000 Monte Carlo simulations to generate a comprehensive distribution of potential portfolio losses.

Risk Metrics Calculation: Calculates and outputs several essential risk metrics:

Value at Risk (VaR) at 95% and 99% confidence levels.

Expected Loss (EL) and Unexpected Loss (UL).

Solvency Ratio, Loss Coverage Ratio, Credit Risk Ratio, and Loss on Default Ratio.

Data Visualization: Generates a histogram of the total loss distribution to provide a clear visual representation of the portfolio's risk profile.

# Methodology
The simulation follows these steps:

# 1. Cholesky Decomposition
Cholesky decomposition is a linear algebra method that allows a symmetric, positive-definite matrix (such as a correlation matrix) to be broken down into a product of a lower triangular matrix and its transpose. In this project, it is used to introduce correlation between random variables, which is essential for simulating realistic credit defaults. If companies are correlated, their probability of defaulting together is higher, which this method allows us to model.

# 2. Monte Carlo Simulation
Monte Carlo simulation is a computational technique used to model the behavior of complex systems by using a large number of random variables. Here, we apply it to simulate 10,000 possible default scenarios. For each scenario, we generate correlated random variables via Cholesky decomposition and determine whether each company defaults. We then calculate the total portfolio loss for that scenario. After 10,000 iterations, we obtain a loss distribution that helps us understand the probability of different loss levels.

# Dependencies
This project requires the following Python libraries:

numpy

scipy

matplotlib

You can install them using pip:

pip install numpy scipy matplotlib

# Usage
Clone this repository to your local machine.

Open the risk-losses-credit-portfolio.ipynb notebook in a Jupyter environment.

Run all cells to execute the simulation, visualize the loss distribution, and display the calculated risk metrics.

# Author
Maïssane Frikh - Mathematical Engineering Student with a focus on quantitative finance and risk modeling.
