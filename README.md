# Modeling Chaos and Different ODEs with Mathematica

**Author:** Edbert Handjaja  
**Email:** EdbertHandjaja2027@u.northwestern.edu

## Abstract
This project investigates chaos theory, focusing on the sensitivity of non-linear dynamical systems to initial conditions, often referred to as the **Butterfly Effect**. Inspired by Edward Lorenz's pioneering work in 1961, this project provides an introduction to chaos theory and explores the modeling of chaotic systems using Mathematica. We dive into different strange attractors, such as Lorenz, Chen, and Dadras, through the lens of Ordinary Differential Equations (ODEs), providing insights into their unpredictable nature.

## Introduction
Chaos theory is a mathematical field that studies the behavior of dynamical systems that are highly sensitive to initial conditions. The focus of this project is to model different chaotic attractors using Mathematica, including the Lorenz attractor, which was discovered by meteorologist Edward Lorenz.

This repository contains Mathematica notebooks and scripts used for modeling chaos and solving differential equations. The chaotic behavior is explored through the Lorenz, Chen, and Dadras attractors.

## Methodology
The models in this project are constructed using the Mathematica software. Key built-in functions used include `NDSolve`, `ParametricPlot3D`, and `SetPrecision`, among others.

### Mathematica Functions Used
- **`NDSolve`**: Used to solve general numerical differential equations.
- **`NDSolveValue`**: Returns specific solutions to the equations.
- **`ParametricPlot3D`**: Generates 3D plots to visualize the chaotic attractors.
- **`SetPrecision`**: Sets precision levels for numerical computations.
- **`PrecisionGoal`** and **`WorkingPrecision`**: Define accuracy and precision levels for results.

### Attractors
- **Non-Chaotic Attractors**: Dynamical systems whose future state can be predicted.
- **Chaotic/Strange Attractors**: Systems whose behavior is sensitive to initial conditions, and thus unpredictable.
### Lorenz Attractor
The Lorenz system models a simplified atmospheric convection and is represented by three non-linear differential equations:
```mathematica
P = 10; R = 28; B = 8/3;
eqns = {x'[t] == P y[t] - P x[t], y'[t] == R x[t] - x[t] z[t] - y[t], z'[t] == x[t] y[t] - B z[t], x[0] == 1, y[0] == 5, z[0] == 10};
sol = NDSolveValue[eqns, {x, y, z}, {t, 0, 100}];
