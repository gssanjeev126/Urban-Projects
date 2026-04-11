# Decentralized Solar Energy Transitions: Belagavi's potential 
##Strategic City Planning Tool

## Author
Sanjeev Gadad. (Specialist - Geospatial Insights, Climate Resilience, Civil Engineer)

## Overview
A city’s true energy potential often lies hidden in plain sight. Project Sun-Drive is an interactive, data-driven dashboard designed to help residential planners and homeowners visualize the impact of solar adoption. By bridging the gap between meteorological data and financial forecasting, it provides a transparent look at the Net Investment, Payback Period, and Carbon Sequestration potential of a single home or an entire community.

## Technical Fundamentals

The dashboard operates on a Quantized Physics Logic. Unlike generic calculators, it enforces real-world constraints:
The 60% Rule: Only 60% of total rooftop area is considered "usable" for panels (accounting for walking space, shading, and tank placement).
Integer Capacity Scaling: Solar capacity is rounded to the nearest integer kW based on a standard 100 sq.ft footprint per 1 kW system.
Dynamic Response UI: Built using a JavaScript-in-HTML architecture, allowing for instantaneous recalculation without a Python backend—ideal for hosting on GitHub Pages.

## Data & Assumptions
### Meteorological Foundation
Location: Belagavi, India.
Annual Yield: Baseline of 1400 kWh/year per 1 kW installed.
Insolation Weights: Factored for the Monsoon Dip (June–August), where generation drops by ~60-65% due to cloud cover.
### Financial Parameters (2025-26 Estimates)
Direct Savings (Self-Consumption): INR 7.50 per unit.
HESCOM Export (Net Metering): INR 2.30 per unit.
Degradation: 0.5% annual loss in panel efficiency.
Tariff Hike: Assumed 3% annual increase in electricity rates.

### Subsidy Structure (PM Surya Ghar)
1-2 kW: INR 30,000 per kW.

3 kW+: Capped at INR 78,000.

### Environmental Impact
Emission Factor: 0.8 kg of CO2 avoided per 1 kWh generated (based on India's coal-heavy grid intensity).
Sequestration Equivalent: One mature tree absorbs approximately 21 kg of CO2 per year.

## How to Run
1. Clone the repository: git clone 
2. Install dependencies
3. Open the notebook in Google Colab or Jupyter and ensure you have authenticated your Earth Engine account.

## Citations & Data Sources
1. Ministry of New and Renewable Energy (MNRE): Operational guidelines for the PM Surya Ghar: Muft Bijli Yojana.
2. KERC (Karnataka Electricity Regulatory Commission): Tariff orders for HESCOM rooftop solar grid integration.
3. NASA POWER Data Access Viewer: Historical solar insolation and meteorological parameters for Belagavi coordinates.
4. IPCC Guidelines for National Greenhouse Gas Inventories: Grid emission factor methodologies for the Indian energy sector.
