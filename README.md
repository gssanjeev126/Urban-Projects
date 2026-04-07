# Belgaum Smart City: Nighttime Light (NTL) & Energy Analytics 
## Overview
This project provides a High-Resolution Temporal Analysis of Belgaum’s urban energy footprint using satellite-derived Nighttime Lights (NTL). By leveraging the NOAA VIIRS (DNB) sensor, we translate raw spectral radiance into actionable municipal metrics, including Grid Consumption (kWh), Fiscal Expenditure (Millions INR), and Carbon Emissions (kg CO2).

The goal is to provide Belgaum Smart City planners with a visual and data-driven baseline for identifying high-density energy zones and potential areas for solar street-lighting transitions.

## Performance Dashboard (Interactive)
The project generates an interactive Area-Spline Hybrid Dashboard that tracks the relationship between urban brightness and fiscal cost.

Blue Zone: Total Grid Demand (kWh)

Red Dotted Line: Carbon Footprint (kg CO2)

Data Callouts: Real-time cost estimation in Millions of INR (M).

## Mathematical Framework
The analysis follows a linear transformation model to convert satellite radiance into municipal energy units:

1. Energy Estimation (kWh)
The total monthly energy is derived from the Sum of Radiance (SoR) over the Region of Interest (ROI):

E(kWh) = ∑(R × A) × κ
Where:
R = Monthly Average Radiance (nW/cm2/sr)
A = Pixel Area (m2)
κ = Luminous Scaling Factor (0.0012)

2. Fiscal Impact (Millions INR)
Cost is calculated based on the standard HESCOM LT-6 (Commercial/Streetlighting) tariff:

Cost (Million Rupees)​ = E (kWh) × 7.00 / 1,000,000
 
3. Environmental Impact (kg CO2)

CO2 = E (kWh) × 0.8 (kg/KWh)

## Data Acquisition: 
Google Earth Engine (EE) API for the NOAA/VIIRS/DNB/MONTHLY_V1/VCMCFG collection.

Geoprocessing: geemap for administrative boundary blending and temporal GIF compositing.

Data Science: Pandas for time-series aggregation and NumPy for fiscal transformations.

Visualization: Plotly for interactive Spline-Area charts (mimicking ggplot2 aesthetics).

## How to Run
1. Clone the repository:
git clone https://github.com/gssanjeev126/Urban-Projects.git

2. Install dependencies:
pip install earthengine-api geemap pandas plotly

3. Open the notebook in Google Colab or Jupyter and ensure you have authenticated your Earth Engine account.

## Citations & Data Sources
Satellite Data: Earth Observation Group, Payne Institute for Public Policy. VIIRS Nighttime Lights Monthly Average Radiance. (https://eogdata.mines.edu/products/vnl/)
Boundary Data: Local Municipality Shapefiles / OpenStreetMap (OSM).
Tariff Source: Hubli Electricity Supply Company Limited (HESCOM) - Schedule of Tariff for FY 2024-25.
