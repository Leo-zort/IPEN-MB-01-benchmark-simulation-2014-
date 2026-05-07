## Description

This repository contains supplementary data and scripts for the study:

> **Non‑monotonic albedo behavior in heavy reflectors: a benchmark study of IPEN/MB‑01 with MCNP5 and Serpent**
> Leonardo Zortea, Pedro Carlos Russo Rossi, Lubianka Ferrari Russo Rossi, Pedro Henrique Silva Rodrigues
> *Submitted to Annals of Nuclear Energy*

The work reexamines the critical loading configurations of the IPEN/MB‑01 research reactor with **carbon steel** and **nickel** reflectors, treating albedo as a thickness‑dependent design variable rather than a fixed boundary condition. Monte Carlo simulations were performed with MCNP5 and Serpent for 36 experimental configurations (18 per material), spanning reflector thicknesses from 0 to approximately 10.5 cm.

---

## Repository Structure

├── cs/ # Figures for carbon steel reflector
│ ├── Eff_albedo(CS).png # Energy‑dependent effective albedo vs thickness
│ ├── Absorption Probability (CS).png # Energy‑dependent absorption probability
│ ├── Scatter Probability (CS).png # Energy‑dependent elastic scattering probability
│ ├── flux_map_cs.svg # Full flux map (all three groups combined)
│ ├── short_flux_map_cs.png # Compact flux map for selected cases
│ ├── thermal_flux_cs.png # Thermal flux distribution inside the reflector
│ ├── epithermal_flux_cs.png # Epithermal flux distribution inside the reflector
│ └── fast_flux_cs.png # Fast flux distribution inside the reflector
├── ni/ # Figures for nickel reflector
│ ├── Plot_eff_(Ni).png # Energy‑dependent effective albedo vs thickness
│ ├── Absorption Probability (Ni).png # Energy‑dependent absorption probability
│ ├── Scatter Probability (Ni).png # Energy‑dependent elastic scattering probability
│ ├── flux_map_ni.png # Full flux map (raster format)
│ ├── flux_map_ni.svg # Full flux map (vector format)
│ ├── thermal_flux_ni.png # Thermal flux distribution inside the reflector
│ ├── epithermal_flux_ni.png # Epithermal flux distribution inside the reflector
│ └── fast_flux_ni.png # Fast flux distribution inside the reflector
├── albedo_with_uncertainty.ods # Albedo values with Monte Carlo statistical uncertainties
├── modelo_py.py # Python script for generating MCNP & Serpent inputs
└── README.md

## File Descriptions

| File / Folder | Content |
|---|---|
| `cs/` | All figures for the **carbon steel** reflector: energy‑dependent albedo curves, absorption and scattering probabilities, and spatially resolved flux maps (thermal, epithermal, fast). |
| `ni/` | Same set of figures for the **nickel** reflector. |
| `albedo_com_uncertainty.ods` | OpenDocument spreadsheet containing the computed total and group‑wise albedo values for all 36 cases, together with the associated Monte Carlo statistical uncertainties (one standard deviation). |
| `modelo_py.py` | Python 3 script that automatically generates MCNP5 and Serpent input decks for any experimental configuration. It reproduces the exact geometry, material compositions, and source definitions used in the benchmark simulations. |

---

## Using the Input Generator (`modelo_py.py`)

The script requires **Python 3** (no external libraries).

### Quick Start

```bash
python modelo_py.py
