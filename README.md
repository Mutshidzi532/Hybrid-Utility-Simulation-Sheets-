# Hybrid-Utility-Simulation-Sheets-
A HOMER Pro configuration model and case study optimising a South African 50MW Solar PV + 40MWh BESS hybrid plant. Evaluates PVsyst AC/DC generation curves against Eskom Megaflex Time-of-Use tariffs to resolve midday inverter clipping constraints and manage battery state-of-charge degradation over a 25-year lifecycle.
# South African 50MW Hybrid Sizing Case Study: PVsyst & HOMER Analysis

A professional technical portfolio documenting a complete engineering simulation and bankable yield assessment for a utility-scale **50 MW Solar PV system** integrated with a **20 MW / 40 MWh Lithium-Ion BESS** operating under South Africa's utility grid constraints.

This project demonstrates the practical application of industry-standard modeling and simulation software to analyse grid-connected hybrid constraints, project degradation parameters, and execute time-of-use economic arbitrage.

---

## 📋 Problem Statement & Objectives

In South Africa, large-scale Independent Power Producers (IPPs) face severe structural and financial inefficiencies due to strict Maximum Export Capacity (MEC) limits at grid connection points and highly volatile Time-of-Use (ToU) tariffs (e.g., Eskom Megaflex). 

The primary objectives of this configuration model are:
1. **System Optimisation Under Constraints:** Forcing a 50 MW solar field, a 40 MWh battery, and a capped 40 MW grid connection to operate smoothly as a unified hybrid power plant.
2. **Revenue Sensitivity Maximisation:** Mapping Eskom's specific high-demand Megaflex tiers to execute automated revenue-shifting dispatch strategies.
3. **Risk Mitigation and Asset Protection:** Restricting deep battery discharges and blocking expensive grid-charging vectors to lower the Levelised Cost of Storage (LCOS).

---

## 🛠️ Software Tool Interoperability & Workflow

This project maps real-world data constraints across a standard energy engineering software pipeline:
1. **PVsyst (Bankable Production Modelling):** Used to define meteorological parameters, module orientation, shading profiles, and calculate exact AC/DC inverter configurations and clipping curves.
2. **HOMER Pro (Microgrid Dispatch Optimisation):** Ingests the raw hourly generation profile from PVsyst to simulate battery degradation, track state-of-charge (SoC) parameters, and calculate overall system economic feasibility.

---

##Repository Structure

*   `homer_config.json` — The master JSON initialization file mapping the exact boundary constraints, system costs, component capacities, and dispatch rules programmed into the HOMER Pro workspace.
*   `pvsyst_generation_profile.csv` — Simulated hourly generation matrix representing a normalized weather database export from the PVsyst variant workspace.

---

##  Eskom Megaflex Tariff Structure Matrix
The model implements the standard high-demand season tariff pricing tiers to determine optimal arbitrage actions within the HOMER dispatch engine:
*   **Peak Windows (R3.60 / kWh):** 07:00–10:00 and 18:00–20:00
*   **Standard Windows (R1.50 / kWh):** 06:00–07:00, 10:00–18:00, and 20:00–22:00
*   **Off-Peak Windows (R0.75 / kWh):** 22:00–06:00
*   [📊 View PVsyst to HOMER Software Data Pipeline](./architecture_diagram.mmd)
👉 [View Full Case Study Report & Optimization Recommendations](./case_study_report.md)

