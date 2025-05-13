# Gravity-Driven Fluid Oscillations in a Drinking Straw

**Abe Garcia — PHYS 381 Final Project**

## Overview

There’s something undeniably compelling about seeing everyday physics come alive — especially when it’s inside something as mundane as a drinking straw. This project explores a deceptively simple experiment: what happens when you submerge a capped straw into a fluid, then suddenly release the cap?

The water doesn’t just rise and stop. It oscillates.

Those oscillations — caused by a mix of hydrostatic pressure, gravity, and damping — form the core of this project. Inspired by Smith and Matlis (2019), I model the motion of the fluid inside the straw using Newton’s second law and explore how well that model aligns with physical intuition, behavior, and simulated results. The project reflects the core ideas of PHYS381: using code, math, and physics together to understand something deeply.

---

## Physics Background

Although the full fluid behavior involves 3D motion and pressure fields, the system’s effective dimensionality can be reduced to one variable: the height of the fluid column inside the straw, $z(t)$, measured from the base. This simplification allows us to treat the system as a nonlinear, damped oscillator with time-varying mass.

Starting from Newton’s second law:

$$
m(z)\ddot{z} + \dot{m}(z)\dot{z} = -mg + \rho g h A - b_0 \dot{z}
$$

With:

* $m(z) = \rho A z$: the fluid mass in the straw
* $\rho$: fluid density
* $A$: straw cross-sectional area
* $h$: submersion depth
* $b_0$: damping constant

This reduces to the second-order ODE:

$$
\ddot{z} = -\frac{\dot{z}^2}{z} + gz - gh + b\dot{z}
$$

I simulate this numerically to observe the dynamics of the fluid column and investigate how damping and initial conditions shape the motion.

---

## Files

* `straw_oscillation.ipynb`: Full code and plots
* `data/simulated_data.csv`: Simulated data
* `figures/oscillation_plot.png`: $z(t)$ plot
* `figures/frequency_spectrum.png`: FFT + Lorentzian
* `report/report.pdf`: Final report (Overleaf)
* `README.md`: This file
