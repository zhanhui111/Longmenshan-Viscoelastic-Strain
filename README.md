
# Viscoelastic Modeling and Strain Rate Benchmarking: Southern Beichuan-Yingxiu Fault

This repository contains the numerical simulation scripts and sample output data for the manuscript: 
**"A viscoelastic model for interseismic deformation and benchmarking of strain rate estimation methods: Southern Beichuan-Yingxiu fault, Longmenshan tectonic belt"** (Submitted to *Geophysical Journal International*).

## 📂 Repository Structure

The repository is organized into two main directories:

### 1. `/scripts`
This folder contains the configuration (`.cfg`) and spatial database (`.spatialdb`) files required to run the 3D finite element simulations using **PyLith**.
* `pylithapp.cfg`: Main PyLith application configuration file.
* `longmen_interseismic.cfg` / `longmen_interseismic_elastic.cfg`: Specific settings for the viscoelastic and pure elastic interseismic models.
* `mat_Longmen_*.cfg` & `mat_Longmen_*.spatialdb`: Material properties and rheological parameters (elastic and Maxwell viscoelastic) for different lithospheric layers (Upper Crust, Lower Crust, Upper Mantle).

### 2. `/sample_data`
This folder contains the extracted surface velocity field results from the 3D finite element models. These datasets were used as the synthetic benchmark for comparing various strain rate estimation methods.
* `Be15surf.xlsx`: Simulated surface velocity field from the **pure elastic model** (15 km locking depth).
* `Bv15surf.xlsx`: Simulated surface velocity field from the **viscoelastic model** (15 km locking depth).

## ⚙️ Requirements

To reproduce the simulations, you need to install the open-source finite element code **PyLith**.
* **PyLith version:** v4.1.3 (or compatible).
* Further installation instructions for PyLith can be found at: [CIG PyLith documentation](https://geodynamics.org/resources/pylith)

## 🚀 Usage

To run the models, navigate to the `/scripts` directory in your terminal and execute PyLith with the desired configuration file. For example, to run the elastic model:

```bash
pylith pylithapp.cfg longmen_interseismic_elastic.cfg
