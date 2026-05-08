# Spatial Optimisation of EV Charging Stations to Address Demand-Supply Mismatch

A spatial data science project analysing the geographic distribution of public EV charging infrastructure across England and developing an optimisation strategy for new station placement in Leeds.

Developed as MSc dissertation project, Urban Data Science and Analytics, University of Leeds (2025).

## Project Overview

This project addresses the spatial mismatch between EV ownership demand and public charging infrastructure supply in England. Using a combination of spatial analysis and location-allocation modelling, it identifies underserved areas and proposes optimal sites for new charging stations in Leeds.

## Methodology

- Kernel Density Estimation (KDE) and Nearest Neighbour Index (NNI) to assess spatial clustering of existing stations across England
- Moran's I for global spatial autocorrelation analysis at regional scale
- Buffer analysis and spatial join operations to evaluate service coverage at LSOA level
- Raster-based overlay using WorldPop 100m population grid to identify demand-supply gaps
- P-median location-allocation optimisation to identify optimal new station sites in Leeds across multiple deployment scenarios

## Data Sources

All datasets used are publicly available under open licences:

- EV charging stations: Open Charge Map (ocm-export, GitHub)
- EV ownership: UK Department for Transport, Vehicle Licensing Statistics (VEH0142)
- Population: ONS 2021 Census; WorldPop 100m raster
- Retail centres: GeoDS UK Open Data Portal
- Job centres: UK Government Journey Time Statistics
- Fuel stations: OpenStreetMap
- Boundary files: ONS Geoportal / OS Data Hub

## Environment

This notebook was developed in Google Colab. File paths (e.g. `/content/`) reflect the Colab environment and should be updated when running locally.

## Dependencies

```python
geopandas, pandas, numpy, matplotlib, seaborn, contextily, scipy, libpysal, esda, shapely, tqdm
```
