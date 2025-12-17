# Numerical Methods & Model Validation in Scientific Computing

This project explores **core numerical methods used in scientific computing**, with an emphasis on **accuracy, stability, and model reliability**.

Through a series of controlled experiments, I investigate:
- numerical approximation errors,
- convergence behavior,
- model verification and validation,
- and the trade-offs between accuracy and computational cost.

All experiments are implemented in Python using NumPy, SciPy, and Matplotlib, with results visualized and discussed directly in Jupyter notebooks.

---

## Project Motivation

In applied mathematics and engineering, **models are approximations**.  
Even when code runs correctly, numerical methods can:
- converge slowly,
- become unstable,
- or give correct answers for the wrong reasons.

This project was created to **systematically study these issues** using well-understood mathematical problems where ground-truth solutions are available.

---

## Topics Covered

### 1. Model Reliability Concepts

Using simplified numerical examples, I demonstrate and distinguish between:

- **Code Verification**  
  Ensuring the numerical implementation matches the intended algorithm.

- **Solution Verification**  
  Checking that numerical solutions converge to the correct answer as resolution improves.

- **Model Validation**  
  Confirming that a model is appropriate for the physical or mathematical problem being solved.

- **Model Calibration**  
  Adjusting model parameters to improve agreement with reference solutions or observations.

These concepts are illustrated with practical examples and failure cases.

---

## Numerical Experiments

### 2. Polynomial vs Piecewise Interpolation

I approximate the Gaussian function:

\[
f(x) = \frac{1}{\sqrt{\pi}} e^{-x^2}
\]

over a finite interval and compare:
- high-degree polynomial interpolation
- piecewise polynomial interpolation (splines)

**Key findings:**
- High-degree global polynomials suffer from oscillations.
- Piecewise interpolation provides more stable and accurate approximations.

---

### 3. Numerical Integration (Quadrature)

The integral of the Gaussian over an infinite domain is known analytically:

\[
\int_{-\infty}^{\infty} f(x)\,dx = 1
\]

I approximate this integral by:
- truncating the infinite domain,
- applying different quadrature rules:
  - Midpoint Rule
  - Trapezoidal Rule
  - Simpson’s Rule

**Analysis includes:**
- error vs number of function evaluations
- convergence rate comparisons
- trade-offs between accuracy and computational cost

---

### 4. ODE Solvers & Convergence Analysis

I solve a time-dependent ordinary differential equation using:
- Forward Euler
- Improved Euler
- Runge–Kutta (RK4)

For each method, I:
- compute numerical error against an exact solution,
- generate log–log convergence plots,
- estimate convergence order using linear regression.

**Key observation:**
Higher-order methods achieve significantly better accuracy at comparable computational cost.

---

## Visualization & Analysis

All experiments include:
- convergence plots
- error vs resolution graphs
- stability diagnostics
- clear annotations explaining observed behavior

Plots are generated using Matplotlib with logarithmic scaling where appropriate.

---

## Tools & Technologies

- **Python**
- **NumPy**
- **SciPy**
- **Matplotlib**
- **Jupyter Notebook**

---



