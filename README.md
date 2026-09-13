# Examining HPC's Environmental Impact (HiMCM)

This repository contains the official research paper submitted to the **High School Mathematical Contest in Modeling (HiMCM)**, where our team was awarded **Honorable Mention**.

## Project Overview & Core Research Questions
High-Performance Computing (HPC) systems are crucial for AI development, but their massive energy consumption poses severe sustainability challenges. This project establishes a Life-Cycle Assessment (LCA) and predictive modeling framework to quantify:
* **Global Energy Consumption:** Total annual electricity usage of HPC systems in 2024.
* **Full-Lifecycle Carbon Footprint:** Embodied (production/disassembly) vs. operational emissions.
* **Future Trends (2025–2030):** Projecting long-term emissions under evolving PUE and GPU upgrades.

## Mathematical Modeling & Methodology

### 1. Component-Level Energy & LCA Model
* **IT Components Breakdown:** Modeled the power of 5 core components (CPUs, GPUs, memory, disk, network) using idle-to-peak differences and utilization rates.
* **PUE Integration:** Multiplied IT energy by the Power Usage Effectiveness (PUE = 1.56) to capture facility-wide overhead.
* **Lifecycle Assessment:** Categorized emissions into three stages (`C_total = C_prod + C_op + C_dis`). Linked facility energy consumption with a globally weighted average carbon intensity, yielding **187.7 million tons of CO2** in 2024.

### 2. Long-Term Forecasting (GM(1,1) & Simulation)
* **PUE Grey Prediction:** Projected the downward PUE trend to **1.379 by 2030** using grey system data smoothing.
* **GPU Upgrade Simulation:** Designed a custom discrete-generation simulation (Algorithm 1) tracking hardware lifespans (5 years max) and quadratic replacement probabilities. Proved that efficiency gains from newer GPUs will drive a net decline in emissions to **116 million tons by 2030**.

## Repository Structure
* `HiMCM_Paper.pdf`: The complete 27-page submission-ready modeling paper.
