# Damped Wave Field Simulation

This repository contains a lightweight C++ simulation of a **2-D damped wave field** solved using explicit finite-difference integration.  
While originally developed for surface-wave experiments, the model is **field-agnostic** and well-suited for studying wave propagation, interference, damping regimes, and boundary interactions.

The simulation outputs per-frame scalar field data, which is visualized offline using Python.

---

## Features

- Explicit time integration of a damped wave equation
- Adjustable grid resolution, damping, wave speed, and timestep
- Reflecting boundary conditions
- Supports wave interference and multi-mode interactions
- Offline 3-D visualization via Matplotlib
- Clean separation between **simulation** and **visualization**

---

## Example Output

Below is an example of wave interference and propagation captured from the simulation:


---

## Code Structure

