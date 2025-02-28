# [AMO] Group Project Schnaufer Drossmann Kraft

# Energy System Optimization with ESS

## Overview

This repository contains the code and data for an optimization study on energy system operations with **Energy Storage Systems (ESS)**. The study investigates the impact of ESS on system flexibility, social welfare, and load fulfillment across different renewable energy scenarios (Stormy, Blue Sky, Cloudy).

This project was developed as part of a university course at the **University of Cologne**.

The repository includes:

- **An optimization model** implemented in **Julia (JuMP)**.
- **Monte Carlo simulations** of wind and solar generation, implemented in **Python**.
- **Precomputed renewable energy data** for running the optimization without rerunning the simulations.
- **Visualizations** of the results.

## Getting Started

### Running the Optimization Model

The `OptimizationModel.ipynb` notebook (written in Julia) models and optimizes the energy system under different renewable scenarios. The required input files (solar and wind energy data) are already provided in the `energy_data/` folder, allowing the model to run out of the box.

#### Setup

1. Install Julia and the required packages if not already installed:

```
import Pkg
Pkg.add(["JuMP", "HiGHS", "DataFrames", "CSV", "Plots"])
```

2. Open `OptimizationModel.ipynb` in a Jupyter notebook or run it in a Julia environment.

### Running the Monte Carlo Simulations

The `monte_carlo/` folder contains Python notebooks that generate synthetic solar and wind power data using Monte Carlo simulations. These simulations create time series data based on historical weather patterns.

## Future Work

This study focuses on a small test system with predefined weather scenarios. Future extensions could include:

- Expanding the network size to more buses and generators
- Implementing stochastic optimization to model forecast uncertainty.
- Evaluating multiple ESS locations and their impact on power flows.
