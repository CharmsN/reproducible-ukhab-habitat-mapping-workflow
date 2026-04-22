# Reproducible UKHab Habitat Mapping Workflow

This repository provides a curated, reproducible workflow for UKHab-aligned habitat classification using a simplified multi-sensor feature set (Sentinel-1, Sentinel-2, and LiDAR), supported by targeted UAV-based label refinement.

---

## Research Design

The workflow follows a staged evaluation framework:

1. **Training Construction (Desborough)**
   Development of the baseline training dataset using UAV-refined polygons.

2. **Schema Extension (Wicksteed)**
   Expansion to additional habitat classes under increased landscape heterogeneity without modification of model parameters.

3. **Cross-site Transfer (Market Harborough)**
   Evaluation of transferability using a fixed model with minimal additional validation.

---

## Method Summary

* Sentinel-2 seasonal NDVI composites (10 m resolution)
* Sentinel-1 VV backscatter (terrain-corrected)
* LiDAR-derived elevation and slope (resampled to 10 m)
* Random Forest classifier (fixed parameters)
* EO → UKHab crosswalk for habitat alignment

---

## Repository Structure

* `notebooks/` – curated workflow notebook
* `scripts/` – preprocessing scripts (including Sentinel-1 SNAP workflow)
* `environment.yml` – simplified environment specification

---

## Data

Raw datasets are not included due to size constraints. Data sources include:

* Copernicus Sentinel-1 and Sentinel-2
* UK National LiDAR Programme

UAV imagery was used for training data refinement and validation only and is not included as part of the predictor feature set.

---

## Reproducibility

This repository is provided as a curated and transparent implementation of the workflow rather than a turnkey software package.

* File paths within the notebook are configured for the original Windows project environment and require modification for use in a different system.
* ESA SNAP (with `esa-snappy`) must be installed and configured separately for Sentinel-1 preprocessing.
* The provided `environment.yml` file represents a simplified dependency specification.

---

## Author

Charmaine Newmarch
MSc Remote Sensing and GIS
