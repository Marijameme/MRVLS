# Minimum Relevant Variables in Linear Systems (MRVLS)

This repository contains an implementation and comparison of several algorithms for solving the **Minimum Relevant Variables in Linear Systems (MRVLS)** problem.

The project was developed as part of the *Algorithms of Artificial Intelligence* course at the Faculty of Mathematics, University of Belgrade.

---

## Problem Description

Given a linear system

\[
Ax = b
\]

the goal is to find a solution vector **x** that satisfies the system while minimizing the number of non-zero elements in **x**.

This optimization problem is known to be **NP-hard**, making exhaustive search infeasible for larger instances.

---

## Implemented Algorithms

### Brute Force

A complete enumeration of all possible subsets of matrix columns.

**Advantages**
- Finds the optimal solution.
- Useful for validating other algorithms.

**Disadvantages**
- Exponential time complexity.
- Practical only for very small instances.

---

### Genetic Algorithm

A population-based evolutionary optimization algorithm.

Implemented features include:

- Tournament selection
- Crossover
- Mutation
- Elitism
- Fitness evaluation based on the number of selected variables and approximation error

The algorithm represents candidate solutions as subsets of matrix columns and evolves them over multiple generations.

---

### Simulated Annealing

A stochastic optimization algorithm inspired by the annealing process in metallurgy.

The implementation includes:

- Binary encoding of selected columns
- Random neighborhood generation
- Temperature-based acceptance criterion
- Fitness evaluation identical to the genetic algorithm


---

## Technologies

- Python 3
- NumPy
- SciPy
- Matplotlib

---

## Results

The algorithms were evaluated on both small and large linear systems.

The experiments show that:

- **Brute Force** guarantees optimal solutions but becomes computationally infeasible as the number of variables increases.
- **Simulated Annealing** performs well on small instances but struggles to find feasible solutions for larger problems.
- **Genetic Algorithm** provides the best balance between solution quality and execution time, successfully solving significantly larger instances.

---

## References

- E. Amaldi, V. Kann – *On the Approximability of Minimizing Nonzero Variables or Unsatisfied Relations in Linear Systems*
- T. Guilmeau et al. – *Simulated Annealing: A Review and a New Scheme*
- A. H. Konstam – *Linear Discriminant Analysis Using Genetic Algorithms*
- Garey & Johnson – *Computers and Intractability*

---

## Author

**Marijana Cupović**

Faculty of Mathematics  
University of Belgrade
