# Urban Mobility Patterns Analysis

![Chicago Transit](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Chicago_Transit_Authority_logo.svg/320px-Chicago_Transit_Authority_logo.svg.png)

## Overview
This project analyzes Chicago Transit Authority (CTA) ridership data to uncover mobility patterns and predict future trends. Using data visualization and machine learning techniques, I've identified station usage patterns, temporal trends, and created forecasting models to support transit planning.

## Key Findings

### Station Usage Patterns
Cluster analysis revealed four distinct types of transit stations based on their weekly usage patterns:

<img src="visualizations/cluster_patterns.png" width="700">

* **Downtown/Business Stations**: High weekday ridership with steep weekend drops
* **Major Transit Hubs**: Extremely high ridership with balanced weekday/weekend usage
* **Mixed-Use Stations**: Medium ridership with moderate weekend drops
* **Neighborhood Stations**: Lower overall ridership with significant weekend drops

### Pandemic Impact & Recovery
The COVID-19 pandemic dramatically affected transit usage, with different patterns of recovery:

<img src="visualizations/yearly_ridership.png" width="700">

The data shows a steady recovery that hasn't yet reached pre-pandemic levels, with distinct seasonal patterns persisting throughout.

### Improved Forecasting
I developed and compared multiple time series forecasting approaches, achieving significant improvements:

<img src="visualizations/lake_state_enhanced_forecast.png" width="700">

The enhanced SARIMA model reduced forecast error by more than 50%, achieving industry-standard "Good" forecast quality with a MAPE of 10.11%.

## Methods Used

* **Data Processing**: Pandas for cleaning and transformation of 1.25+ million records
* **Visualization**: Matplotlib, Seaborn, and Plotly for static and interactive visualizations
* **Machine Learning**: K-means and hierarchical clustering for station pattern identification
* **Time Series Analysis**: SARIMA modeling for ridership forecasting with model selection via AIC

## Repository Structure
```
urban_mobility_analysis/
├── urban_mobility_analysis.ipynb  # Main analysis notebook
├── data/                          # Dataset folder
├── visualizations/                # Generated visualizations
├── forecast_evaluation.md         # Detailed forecast analysis
└── requirements.txt               # Required packages
```

## Key Visualizations

### Day-of-Week Patterns
The heatmap below shows how ridership varies by day of week across top stations:

<img src="visualizations/dow_heatmap.png" width="700">

### Geographic Distribution
Interactive visualization of stations by type (available in the repository):

<img src="visualizations/map_preview.jpg" width="700">

## Setup and Usage

```bash
# Clone the repository
git clone https://github.com/yourusername/urban-mobility-analysis.git

# Navigate to project directory
cd urban-mobility-analysis

# Install required packages
pip install -r requirements.txt

# Open the notebook
jupyter lab urban_mobility_analysis.ipynb
```

## Future Work
- Incorporate weather data and special events for improved forecasting
- Analyze neighborhood demographics in relation to transit patterns
- Develop more sophisticated deep learning models for long-term prediction

## Dataset
This analysis uses the Chicago Transit Authority (CTA) ridership dataset, which provides daily entry totals for each station in Chicago's "L" train system from 2001-2024.