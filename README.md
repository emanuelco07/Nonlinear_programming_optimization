# Nonlinear Programming Optimization: Cylindrical Tank Design

This repository contains the mathematical modeling, analysis, and algorithmic implementation for a nonlinear optimization problem focused on industrial design efficiency.

## Problem Description

The project addresses the design of a cylindrical storage tank with a fixed volume of $500 m^3$. The objective is to minimize the total construction cost, which is determined by the surface area of the materials used for the base and the lateral wall.

### Objectives and Constraints
* [cite_start]**Objective Function**: Minimize the cost function $f(r, h) = 2 \cdot \pi \cdot r^2 + 2 \cdot \pi \cdot r \cdot h$[cite: 13, 14].
* [cite_start]**Equality Constraint**: The volume must be exactly $500 m^3$, defined by $g(r, h) = \pi \cdot r^2 \cdot h = 500$[cite: 15, 16].
* [cite_start]**Variables**: The radius ($r$) and height ($h$) of the cylinder[cite: 11, 12].

## Technical Implementation

The project explores the problem using various mathematical and computational methods:

### 1. Mathematical Characterization
[cite_start]The problem is classified as a nonlinear, static, and parametric optimization with equality constraints[cite: 18, 19, 21]. [cite_start]It is further identified as a convex programming problem because the objective function is convex and the feasible set is defined by a consistent equality[cite: 24, 25].

### 2. Analytical Solution (Lagrange Multipliers)
[cite_start]The global optimum was determined analytically using the Lagrange Multipliers method[cite: 27]. 
* [cite_start]**Lagrangian Function**: $L(r, h, \lambda) = 2\pi r^2 + 2\pi rh + \lambda(\pi r^2 h - 500)$[cite: 29].
* [cite_start]**Optimal Dimensions**: Radius $r \approx 4.301$ m and Height $h \approx 8.602$ m[cite: 31, 32].
* [cite_start]**Minimum Surface Area**: $\approx 348.73 m^2$[cite: 33].

### 3. Computational Solvers (SciPy)
[cite_start]The problem is implemented in Python using the `scipy.optimize.minimize` library, specifically utilizing the **SLSQP** (Sequential Least Squares Programming) algorithm to handle the nonlinear constraints[cite: 35, 41].

### 4. Search Algorithms
To compare performance against the exact solver, the project includes:
* [cite_start]**Hill Climbing**: A local search algorithm adapted for continuous variables to find the minimum cost area[cite: 46].
* [cite_start]**Simulated Annealing**: A metaheuristic approach used to navigate the nonlinear search space and avoid local optima[cite: 48].

## Results Summary

| Method | Radius (r) | Height (h) | Minimized Area |
| :--- | :--- | :--- | :--- |
| **Analytical (Lagrange)** | 4.301 m | 8.602 m | 348.73 m² |
| **SciPy Solver** | 4.301 m | 8.602 m | 348.73 m² |

## Documentation
For the full theoretical breakdown, including the Karush-Kuhn-Tucker (KKT) conditions and detailed search space analysis, please refer to the Romanian documentation:

[Read Documentation (Romanian)](TO_NLP_Cosereanu_Emanuel_problema_1.pdf)

## Author
Coșereanu Emanuel
INFO, Year 3, Group 40322
[cite_start]Oil & Gas University of Ploiești [cite: 3]
