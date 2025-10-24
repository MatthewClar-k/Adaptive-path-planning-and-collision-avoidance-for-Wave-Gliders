# Adaptive Path Planning and Collision Avoidance for Wave Gliders

This repository contains all MATLAB code developed as part of the **EEE4022S Final Year Project** at the **University of Cape Town**, titled:

> **Adaptive Path Planning and Collision Avoidance for Wave Gliders**

Supervisors: **A/Prof. R.A. Verrinder** and **Dr. S. Nicholson (CSIR SOCCO)**

---

## Overview

This project investigates autonomous path planning and collision avoidance strategies for **Wave Gliders** operating in dynamic maritime environments.  
It is divided into three main components:

1. **Global Path Planning**  
2. **Local Path Planning**  
3. **Collision Avoidance**

Each section contains MATLAB Live Scripts (`.mlx`) and functions designed to simulate, visualise, and analyse autonomous navigation under different environmental and operational conditions.

---

## 1. Global Path Planning

### Files
- `Global_Path_Planning.mlx` — Contains the three main test scenarios for evaluating the global path planning algorithm.  
- `Parameter_Modifications.mlx` — Demonstrates the effect of modifying key planner parameters on overall performance.

### Description
The global path planner determines an optimal route from a start to a goal position over a large-scale environment.  
Different test environments were used to evaluate path optimality, coverage, and sensitivity to parameter changes.

---

## 2. Local Path Planning

### Files
Eight separate scripts correspond to specific simulation scenarios, each testing a different environmental or dynamic condition:

1. `apf_local_minimum.m` — Local minimum test  
2. `apf_no_current.m` — No current scenario  
3. `apf_constant_current.m` — Constant current environment  
4. `apf_eddy_current.m` — Eddy current environment  
5. `apf_single_dynamic_obstacle.m` — Single dynamic obstacle  
6. `apf_multiple_dynamic_obstacles.m` — Multiple dynamic obstacles  
7. `apf_complex_constant_current.m` — Complex environment with constant current  
8. `apf_complex_eddy_currents.m` — Complex environment with eddy currents  

### Description
These scripts implement an **Artificial Potential Field (APF)**-based local path planning algorithm, enhanced to account for **Wave Glider dynamics** (average speed and turning radius) and **environmental ocean currents**.  
The scenarios test the planner’s ability to generate smooth, feasible paths under realistic constraints and to handle local minima and moving hazards.

---

## 3. Collision Avoidance

### Files
Each motion type tested has two corresponding files:

- **Straight trajectory:**  
  - `Straight.mlx`  
  - `Straight_ELLIPSE.mlx`

- **Curved trajectory:**  
  - `Curved.mlx`  
  - `Curved_ELLIPSE.mlx`

- **Varying trajectory:**  
  - `Varying.mlx`  
  - `Varying_ELLIPSE.mlx`

### Description
These scripts evaluate the performance of an **AIS-based dynamic collision avoidance** system using simulated vessel trajectories.  
Each motion profile (straight, curved, varying) models how the Wave Glider predicts potential collisions and adjusts its course accordingly.  
The `_ELLIPSE` scripts generate **uncertainty funnels (ellipses)** to visualise prediction confidence regions and assess risk dynamically.

---

## Summary

| Component | Purpose | Key Output |
|------------|----------|------------|
| Global Path Planning | Generate optimal long-range routes | Path efficiency, parameter sensitivity |
| Local Path Planning | Navigate locally with environmental adaptation | Feasible WG paths, obstacle avoidance |
| Collision Avoidance | Predict and avoid dynamic maritime traffic | Risk assessment, uncertainty modelling |

---

## Tools & Environment

- **Software:** MATLAB R2024b or later  
- **Toolboxes:** Navigation Toolbox, Robotics System Toolbox, Mapping Toolbox  
- **Platform:** Tested on Windows 11 (64-bit)

---

## Citation

If you reference this work, please cite:

> Clark, M. (2025). *Adaptive Path Planning for Wave Gliders: AIS-Based Dynamic Collision Avoidance.*  
> BSc(Eng) Final Year Project, University of Cape Town, South Africa.

---

## Author

**Matthew Clark**  
Department of Electrical Engineering  
University of Cape Town  
[matt.clark514@gmail.com](mailto:matt.clark514@gmail.com)

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
