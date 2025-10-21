# Satellite Visibility Check Using Space-Based Tracker

This repository contains the implementation for simulating satellite visibility from a space-based tracker. The notebook performs orbital propagation, field-of-view calculations, sunlight and range filtering, and identifies entry/exit visibility events over a 24-hour period.

---

## Files
- **Satellite_Visibility_Analysis.ipynb** — Main Jupyter Notebook containing code and results.  
- **requirements.txt** — List of Python dependencies.

---

## How to Run
1. Clone or download the repository.  
2. Install required libraries:
   ```bash
   pip install -r requirements.txt
3. Digantara - MDE Assignment (Q1).ipynb
4. Open the notebook in JupyterLab or Jupyter Notebook.

---

## Description 
The notebook performs the following steps:
1. Propagates satellite orbit using TLE data with the SGP4 model.
2. Propagates the tracker orbit using Poliastro.
3. Computes the field-of-view (30° cone) and checks geometric alignment.
4. Applies range (<1000 km) and sunlight conditions for visibility.
5. Detects start and end times of visible intervals and outputs results.

---

## Dependencies 
1. numpy
2. sgp4
3. astropy
4. poliastro
5. matplotlib

---

## Notes
1. Time step used: 60 seconds for a 24-hour simulation.
2. Earth modeled as spherical, atmospheric effects neglected.
3. Tracker points along its velocity vector.
4. TLE data assumed valid within ±1 day of epoch.
