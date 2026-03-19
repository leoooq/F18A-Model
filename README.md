# F18A Simulink 6DOF Model

A 6-DOF nonlinear flight dynamics model of the F/A-18A implemented in Simulink, with the aircraft dynamics written as a **C-MEX S-Function** and integrated into a Simulink simulation framework.

## Overview

This project provides a Simulink-based F/A-18A six-degree-of-freedom model for simulation and control design.

The model uses:

- a **C-MEX S-Function** for the aircraft rigid-body / aerodynamic dynamics
- a **Simulink model** for signal routing, actuator blocks, simulation setup, and visualization

## Inputs and Outputs

### Inputs (4)

The model takes four control inputs:

- `de` — elevator deflection
- `da` — aileron deflection
- `dr` — rudder deflection
- `T` — thrust

### Outputs (15)

The model outputs the following 15 variables:

- `xa, ya, za` — inertial positions
- `V, chi, gamma` — speed, heading angle, flight-path angle
- `alpha, mu, beta` — angle of attack, bank-related angle, sideslip angle
- `p, q, r` — body angular rates
- `phi, theta, psi` — Euler angles

## Project Structure

Typical files in this repository:

```text
F18A_6DOF_CMEX_Model.slx      Simulink model
F18_HARV_6DOF_cmex.c          C-MEX S-Function source code
build_cmex.m                  MATLAB script for compiling and building the model
