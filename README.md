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

![scalar-wave-field](https://github.com/user-attachments/assets/9008389d-ad5e-44e9-84aa-434df912f78b)

---

## Code Structure

At present, the simulation is intentionally minimal and self-contained. All core logic lives in a single source file while the physics model is being validated and tuned.

src/
    main.cpp # Damped scalar wave simulation (field evolution + CSV output)
visualize.py # Offline visualization of CSV frames (3D surface animation)
output/ # Generated per-frame CSV files (not committed)


The solver evolves a 2-D scalar field using a damped wave equation with explicit time integration. Simulation behavior (propagation speed, damping, and oscillation regime) is controlled entirely through parameters defined at the top of `main.cpp`.

In particular, increasing the order of magnitude of `disturb_amp` produces larger initial velocity impulses and results in more visibly pronounced wave heights in the visualization, while smaller values lead to subtler surface motion.

