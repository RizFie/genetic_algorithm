# Evolutionary PID Tuning for Robotics System: Drone Altitude Control

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RizFie/genetic_algorithm/blob/main/pid_optimizer_ga.ipynb)

This repository demonstrates the use of a Custom Genetic Algorithm (GA) to automatically optimize the Proportional, Integral, and Derivative (PID) gains for a simulated Unmanned Aerial Vehicle (UAV).

## The Objective
Manually tuning a PID controller is time-consuming and often results in sub-optimal performance. This project applies evolutionary optimization to find the optimal $K_p, K_i$, and $K_d$ parameters to minimize a drone's flight error (using the Integral of Squared Error) when trying to reach and maintain a 10-meter setpoint.

## Architecture
* **The Optimizer:** A Genetic Algorithm built from scratch featuring tournament selection, single-point crossover, and bit-flip mutation using continuous binary chromosome encoding.
* **The Environment:** A lightweight, 1D physics simulation calculating drone thrust, simulated physics, and positional error.

## Results
The GA successfully converged on highly aggressive Proportional gains while minimizing Derivative dampening, resulting in a rapid ascent to the target altitude.
* **Optimal Kp:** 9.96
* **Optimal Ki:** 0.00
* **Optimal Kd:** 0.02

## How to Run

### Option 1: Run in Browser (Recommended)
Click the **"Open in Colab"** badge at the top of this page to run the simulation directly in your browser without any setup.

### Option 2: Run Locally
1. Clone the repository: 
   ```bash
   git clone [https://github.com/RizFie/genetic_algorithm.git](https://github.com/RizFie/genetic_algorithm.git)
