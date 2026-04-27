# Nonlinear Programming Optimization

This repository contains the implementation of several optimization techniques applied to a specific industrial problem: minimizing harmful emissions during the mixing process of two petroleum products at a refinery.

The project includes a theoretical analysis of the objective function, mathematical modeling, and a performance comparison between exact solvers, iterative methods, and heuristic algorithms.

## Problem Definition

The goal is to minimize the emission function:
**f(t1, t2) = ln(2^t1 + 2^t2)**

Subject to the following constraints:
*   -0.4 <= t1 <= 2 (Temperature of the first product)
*   3.2 <= t2 <= 10 (Temperature of the second product)
*   t1 + t2 >= 4.5 (Minimum combined temperature threshold)

The problem is characterized as a mathematical, static, constrained, nonlinear, and convex optimization problem.

## Implemented Methods

The project evaluates three different approaches to find the global optimum:

1.  **PySCIPOpt (Exact Solver)**: Used as a benchmark to identify the exact mathematical optimum at the constraint boundary.
2.  **Newton's Method with Restarts**: A second-order optimization technique that utilizes the Hessian matrix and first-order derivatives. It includes a restart mechanism to explore the search space.
3.  **Simulated Annealing**: A probabilistic heuristic inspired by metallurgy, used to find an approximate global optimum in a continuous search space without requiring derivatives.

## Key Features

*   **Mathematical Analysis**: Includes the calculation of first and second-order derivatives and verification of the Hessian matrix to prove convexity.
*   **Visualizations**: Link to 3D graphical representations of the objective function and the feasible region.
*   **Comparative Analysis**: A detailed comparison of results, showing that the optimum lies exactly on the t1 + t2 = 4.5 constraint boundary.

## Documentation

For a detailed theoretical explanation and step-by-step mathematical proof, please refer to the full documentation written in Romanian:

[Read the Romanian Documentation (PDF)](TO_NLP_Cosereanu_Emanuel_problema1.pdf)

## Requirements

The implementation requires Python 3.x and the following libraries:
*   NumPy
*   PySCIPOpt
*   Matplotlib (for local visualizations)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/emanuelco07/Nonlinear_programming_optimization.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Nonlinear_programming_optimization
   ```
3. Run the main script:
   ```bash
   python Main.py
   ```

## Author
Emanuel Coșereanu
INFO Year 3, Group 40322
University of "Petrol – Gaze", Ploiești
