# Population Stability and Sex Ratios: A Mathematical Perspective

## Overview
This project models the population dynamics and sex-ratio behavior of sea lampreys using a system of ordinary differential equations. The model studies how resource availability affects total population size, resource depletion/regeneration, and the male-to-female sex ratio over time.

The main goal is to understand how scarce versus abundant resources influence sea lamprey population stability and long-term equilibrium behavior.

## Model Description
The model tracks three main quantities:

- `N`: total sea lamprey population
- `R`: available environmental resources
- `S`: male sex ratio

The population model is based on logistic growth with resource dependence. Birth rates depend on the female proportion of the population, while mortality is proportional to total population size. The resource equation includes both regeneration and consumption by the lamprey population. The sex-ratio function changes with resource availability, where scarce resources increase the male ratio and abundant resources favor a higher female proportion.

## Main Equations

The model uses the following system:

- Population dynamics:
  `dN/dt = rN(1 - S)(1 - N/K)(R/Rmax) - mN`

- Resource dynamics:
  `dR/dt = beta(Rmax - R) - deltaNR`

- Sex ratio:
  `S(R) = smax - (smax - smin)(R/Rmax)`

## Parameters
Important parameters include:

- `r`: population growth rate
- `K`: carrying capacity
- `m`: mortality rate
- `beta`: resource regeneration rate
- `delta`: resource consumption rate
- `Rmax`: maximum resource level
- `smin`: minimum male sex ratio
- `smax`: maximum male sex ratio

## Experiments
The project compares two main resource scenarios:

1. **Scarce resources**
   - Lower resource maximum
   - Higher resource consumption
   - Slower population growth
   - Higher male sex ratio

2. **Abundant resources**
   - Higher resource maximum
   - Faster resource regeneration
   - Population approaches carrying capacity
   - Lower male sex ratio, meaning a higher female proportion

A stochastic version of the model is also tested by adding random noise to the population equation.

## Results
The model shows that resource availability strongly affects both population growth and sex ratio. Under scarce resources, the population stabilizes below carrying capacity and the male sex ratio approaches its upper bound. Under abundant resources, the population grows closer to carrying capacity and the female proportion increases.

The stochastic simulations suggest that the model is relatively robust because random perturbations do not substantially change the overall population trajectory.

## Files
- `Math_Modeling_MCM.pdf`: final written report
- `MCM.ipynb`: simulation and plotting code

## How to Run
1. Clone or download this repository.
2. Open the notebook script.
3. Install the required packages:

```bash
pip install numpy matplotlib scipy
