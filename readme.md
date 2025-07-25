# Reinforcement Learning in a Gridworld Environment

This repository contains a Python implementation of several reinforcement learning algorithms applied to a classic 5×5 gridworld problem. The project demonstrates and compares model-based (Dynamic Programming) and model-free (Monte Carlo) methods for finding optimal policies.

> **Note:**
> The entire solution is provided within a single, commented Jupyter/Colab notebook (`Assignment2.ipynb` or `Assignment2.html`).

## Project Overview

The project is divided into two main parts, each exploring a unique version of the gridworld:

### Part 1: Dynamic Programming

- **Environment:**
A 5×5 grid with special states that provide rewards and cause deterministic or stochastic teleportations.
- **Objective:**
To calculate the value function for a given policy and to find the optimal policy using methods that require full knowledge of the environment's dynamics.


### Part 2: Monte Carlo Methods

- **Environment:**
The gridworld is modified to be episodic, introducing terminal states and adjusted step rewards.
- **Objective:**
To find the optimal policy using model-free methods that learn directly from episodes of experience—without assuming prior knowledge of the environment's transitions or rewards.


## Algorithms Implemented

This project provides implementations for the following fundamental reinforcement learning algorithms:

### Dynamic Programming (Part 1)

- **Policy Evaluation**
    - Direct solution via matrix inversion
    - Iterative Policy Evaluation
- **Optimal Policy Search**
    - Policy Iteration
    - Value Iteration


### Monte Carlo Methods (Part 2)

- **On-Policy Control**
    - MC with Exploring Starts
    - MC with ε-soft Policies
- **Off-Policy Control**
    - Off-Policy MC with Importance Sampling


## Requirements

The code is written in Python 3 and requires the following libraries:

- `numpy`
- `matplotlib`
- `seaborn`
- `tqdm`

You can install all dependencies via pip:

```bash
pip install numpy matplotlib seaborn tqdm
```


## How to Run

The easiest way to run the notebook is with Google Colab (no local setup required):

1. **Open in Colab:**
Upload the `Assignment2.ipynb` notebook to [Google Colab](https://colab.research.google.com/).
2. **Execute the Code:**
Run the notebook cells sequentially from top to bottom.
3. **View Results:**
The notebook will output explanations, value function plots, policy diagrams, and summary insights for each part.

## Results Summary

- All implemented algorithms—both model-based and model-free—successfully converge to the same logical, optimal policy: **navigate toward the highest-reward state (the blue square) as efficiently as possible**.
- **Dynamic Programming** methods, given access to the environment's full model, find the optimal policy quickly and precisely.
- **Monte Carlo** methods learn the same strategy through repeated episodes of experience; the off-policy variant takes significantly more episodes to converge, highlighting trade-offs in sample efficiency between different approaches.

Feel free to use or adapt the notebook for your own studies or experiments with classic reinforcement learning algorithms.

