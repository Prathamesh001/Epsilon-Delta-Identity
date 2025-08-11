# Epsilon-Delta Identity Verification

## Introduction

This repository contains a simple Python script designed to verify the **Epsilon-Delta Identity**, a fundamental relationship in tensor calculus. The identity relates the Levi-Civita symbol ($\epsilon_{ijk}$) to the Kronecker delta ($\delta_{ij}$). This script systematically checks the identity for every possible combination of indices in a 3-dimensional space.

The Epsilon-Delta Identity is a powerful tool used extensively in fields like structural mechanics and continuum mechanics to simplify complex tensor expressions. It is particularly useful for working with cross products in vector algebra and for deriving key equations in physics and engineering.

## The Identity

The identity is given by the formula:

$$\epsilon_{ijk} \epsilon_{imn} = \delta_{jm} \delta_{kn} - \delta_{jn} \delta_{km}$$

The script verifies that for every combination of the free indices $j, k, m, n$, the summation over the repeated index $i$ on the left-hand side always equals the expression on the right-hand side.

## Code Description

The script is composed of two primary functions and a main verification loop:

### 1. `epsilon(i, j, k)`

This function calculates the value of the **Levi-Civita symbol** for a given set of indices.
* Returns `1` for even permutations of (1, 2, 3), such as (1, 2, 3), (2, 3, 1), and (3, 1, 2).
* Returns `-1` for odd permutations, such as (3, 2, 1), (1, 3, 2), and (2, 1, 3).
* Returns `0` if any two indices are the same.

### 2. `delta(a, b)`

This function calculates the value of the **Kronecker delta**.
* Returns `1` if the indices `a` and `b` are equal.
* Returns `0` if the indices are not equal.

### 3. Main Verification Loop

The main part of the script uses nested loops to iterate through all possible combinations of the free indices `j`, `k`, `m`, and `n` from 1 to 3. For each combination, it:
1.  Calculates the left-hand side (**LHS**) by summing the product `epsilon(i, j, k) * epsilon(i, m, n)` over `i` from 1 to 3.
2.  Calculates the right-hand side (**RHS**) using the `delta` function: `delta(j, m) * delta(k, n) - delta(j, n) * delta(k, m)`.
3.  Prints both results to demonstrate that `LHS == RHS`.

## How to Run

To run this script, simply save the code in a file named `epsilon_delta_verification.py` and execute it from your terminal:

```bash
python epsilon_delta_verification.py
```

## Acknowledgments

This assignment was completed under the guidance of **Prof. Chandu Parimi**.

## Contact Information

Name: Prathamesh Varma\
Phone: +91 7219204543\
E-mail: prathamesh66523@gmail.com\
Student: BITS Pilani Hyderabad Campus

---
*README generated with assistance from AI.*
