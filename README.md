# PACS Challenge 1

This project is a part of the Advanced Programming for Scientific Computing course at Politecnico di Milano. The goal of the project is to develop an iterative solver that computes the following:

![formula](https://latex.codecogs.com/svg.image?x=\underset{y\in\mathbb{R}^n}{\mathrm{argmin}}\,f(y))

## Introduction

Given an initial guess $x_0$, at every time step the algorithm computes:

$$x_{k+1} = x_k - \alpha_k \nabla f(x_k), \qquad k = 1, \ldots, k_{\max}$$

Where $\alpha_k$ is computed depending on the chosen method (Exponential decay, Inverse decay, or Armijo).

## How to use

To use this project, follow these steps:

1. Clone the repository:
```bash
   git clone https://github.com/mikyPolimi/PACS_Challenge_1.git
   cd PACS_Challenge_1
```

2. (**Only if you want to modify the default choices**)

   Go into `parameter.hpp` and select:
   - Function to minimize
   - Method for computing $\alpha$ (Exponential, Inverse, Armijo)
   - Parameters for the selected method ($\mu$ for Exponential and Inverse, $\sigma$ for Armijo)
   - Stopping criteria parameters:
     - Step length tolerance $\varepsilon_s$
     - Residual tolerance $\varepsilon_r$
     - Maximum number of iterations $k_{\max}$
   - Initial values:
     - $\alpha_0$ (initial step size)
     - $x_0$ (initial guess)

3. Run the code:
```bash
   make
   ./main
```
