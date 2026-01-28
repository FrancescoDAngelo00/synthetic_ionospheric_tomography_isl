# Synthetic Ionospheric Tomography with Multi-GNSS ISL

This repository contains the Python code used to generate synthetic data and perform numerical simulations for the study:

**Exploiting multi-GNSS constellation Inter-Satellite Link for stabilizing ionospheric tomographic reconstruction.**

The code reproduces a realistic synthetic ionospheric environment and simulates tomographic reconstruction using multi-GNSS Inter-Satellite Links (ISL). It is structured into four main folders, each corresponding to a step in the simulation pipeline.

---

## Repository Structure

### 1. `estrazione_dati_orbitali_e_isl`
- Creates the synthetic ionospheric region for the simulation.
- Defines days and time intervals to analyze.
- Reproduces satellite positions for Galileo and GPS in the selected intervals.
- Defines a discrete ionosphere with electron density values provided by IRI Model 2016.
- Contains Jupyter notebooks (`.ipynb`) to run the simulations and a folder with produced data (`DATI` or `RISULTATI`).

### 2. `creazione_matrici_di_adiacenza`
- Simulates the STEC data acquisition process for:
  - Satellite-to-ground links
  - Inter-satellite links
- Incorporates a grid of ground stations and temporal aggregation windows.
- Processes two cases: **noise-free** and **noisy**.
- Constructs the adjacency matrices for the tomographic system for each configuration.

### 3. `inversione_sistema_lineare_NO_noise`
- Inverts the linear systems generated in the noise-free case.
- Produces reconstructed solutions.
- Generates figures corresponding to the results presented in the paper.

### 4. `inversione_sistema_lineare_SI_noise`
- Inverts the linear systems for the noisy case.
- Produces reconstructed solutions.
- Generates figures corresponding to the results presented in the paper.

---

## Usage

1. Python 3.9+ is recommended.
2. Install required packages via:

```bash
pip install -r requirements.txt

## Citation
If you use this code, please cite:
