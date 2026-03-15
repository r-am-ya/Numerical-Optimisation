# Numerical-Optimisation

# Interior-Point Method for Linearly Constrained Convex Optimization
## Project Overview

This project demonstrates how different optimization algorithms solve a linearly constrained convex optimization problem. The objective is to minimize a quadratic function while satisfying a linear constraint.

Three optimization algorithms are implemented and compared:

- Gradient Descent (GD)

- Projected Gradient Descent (PGD)

- Interior-Point Method (IPM)

The project analyzes how each algorithm converges to the optimal solution and how constraints influence the optimization process.

## Problem Formulation

The optimization problem solved in this project is:

Minimize:
f(x)=x1^2​ + x2^2

Subject to: x1^2 + x2^2 ≤ 1

Where x=(x1​,x2​) are decision variables.

The objective function is convex, ensuring that a global minimum exists within the feasible region.

## Algorithms Implemented
### 1. Gradient Descent

Gradient Descent iteratively updates the solution in the direction opposite to the gradient of the objective function.

Update rule: xk+1​=xk​−α∇f(xk​)

This method does not consider constraints.

### 2. Projected Gradient Descent

Projected Gradient Descent ensures the solution stays within the feasible region.

Steps:

- Perform gradient update.

- Check if constraint is violated.

- Project solution back into feasible region.

### 3. Interior-Point Method

The Interior-Point Method handles constraints using a barrier function.

Modified objective function: F(x)=f(x)−μlog(1−x1​−x2​)

This prevents the solution from crossing the constraint boundary.

## Implementation

The project is implemented in Python using the following libraries:

- NumPy – numerical computations

- Matplotlib – visualization of convergence and optimization paths

The implementation includes:

- Definition of objective function

- Gradient calculation

- Constraint function

- Three optimization algorithms

- Convergence visualization

- Optimization path visualization

## Results

The project generates two types of visualizations:

### Convergence Graph

Shows how the objective value decreases over iterations for each optimizer.

### Optimization Path Graph

Shows the path taken by each algorithm in the (x1​,x2​) plane relative to the constraint boundary.

These graphs help analyze:

- convergence speed

- stability

- constraint handling

## Applications

Interior-point methods are widely used in:

- Machine Learning optimization

- Linear Programming

- Support Vector Machines

- Resource allocation problems

- Portfolio optimization
