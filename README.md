# Reproducible UKHab Habitat Mapping Workflow

This repository provides a reproducible workflow for UKHab-aligned habitat classification using a minimal multi-sensor feature set (Sentinel-1, Sentinel-2, and LiDAR), supported by targeted UAV-based label refinement.

## Research Design
The workflow follows a staged evaluation framework:

1. **Training Construction (Desborough)**  
   Development of the baseline training dataset using UAV-refined polygons.

2. **Schema Extension (Wicksteed)**  
   Expansion to additional habitat classes under increased landscape heterogeneity without changing model parameters.

3. **Cross-site Transfer (Market Harborough)**  
   Evaluation of transferability using a fixed model and minimal additional validation.

## Method Summary
- Sentinel-2 seasonal NDVI composites (10 m)
- Sentinel-1 VV backscatter (terrain-corrected)
- LiDAR-derived elevation and slope (resampled to 10 m)
- Random Forest classifier (fixed parameters)
- EO → UKHab crosswalk for habitat alignment

## Repository Structure
- `notebooks/` – main workflow (`workflow.ipynb`)
- `scripts/` – preprocessing scripts
- `environment.yml` – reproducible environment specification

## Data
Raw datasets are not included due to size constraints. Data sources:
- Copernicus Sentinel-1 and Sentinel-2
- UK National LiDAR Programme

## Reproducibility
The workflow is designed to be reproducible using open-source tools and publicly available data. The environment file allows full reconstruction of the processing environment.

## Author
Charmaine Newmarch  
MSc Remote Sensing and GIS
