🌍 Multi-Temporal Vegetation, Temperature, and Rainfall Analysis (1988–2024)

## Overview

This project presents a comprehensive geospatial analysis of vegetation dynamics, land surface temperature (LST), and rainfall variability over Varanasi, India, using multi-temporal satellite and climate datasets. The study integrates Landsat imagery (1988–1994, 2014–2024) and CHIRPS rainfall data (1981–2024) to examine long-term environmental changes and climate–vegetation interactions.

The workflow combines remote sensing, spatial analysis, and time-series modeling to generate consistent seasonal datasets for vegetation indices (NDVI, SAVI), temperature, and precipitation.

---

## Objectives

* Analyze long-term trends in vegetation health using NDVI and SAVI
* Quantify seasonal and inter-annual variability in land surface temperature
* Assess rainfall patterns and their relationship with vegetation dynamics
* Develop a consistent multi-decadal geospatial analysis framework

---

## Study Area

**Varanasi, India**
A rapidly urbanizing region in the Indo-Gangetic Plain, characterized by strong seasonal climate variability and significant land use changes.

---

## Data Sources

| Dataset         | Source | Period    | Resolution |
| --------------- | ------ | --------- | ---------- |
| Landsat 5 TM    | USGS   | 1988–1994 | 30 m       |
| Landsat 8 OLI   | USGS   | 2014–2024 | 30 m       |
| Landsat 9 OLI   | USGS   | 2021–2024 | 30 m       |
| MODIS LST       | NASA   | 2000–2024 | 1 km       |
| CHIRPS Rainfall | UCSB   | 1981–2024 | ~5 km      |

---

## Methodology

### Preprocessing

* Surface Reflectance scaling (Landsat Collection 2 L2)
* Cloud, shadow, and cirrus masking using QA_PIXEL
* Spatial clipping to Area of Interest (AOI)

### Vegetation Indices

* **NDVI** = (NIR − Red) / (NIR + Red)
* **SAVI** = ((NIR − Red) / (NIR + Red + L)) × (1 + L), where *L = 0.5*
* Threshold applied: **≥ 0.23** for vegetation filtering

### Temporal Aggregation

* Seasonal classification:

  * Winter (Jan–Feb)
  * Pre-Monsoon (Mar–May)
  * Monsoon (Jun–Sep)
  * Post-Monsoon (Oct–Dec)
* Multi-year seasonal compositing and averaging

### Land Surface Temperature (LST)

* Derived from Landsat L2 thermal bands and MODIS LST products
* Converted to Celsius using scale factors
* Annual aggregation for long-term trend analysis

### Rainfall Analysis

* CHIRPS daily data aggregated to seasonal totals
* Spatial averaging over AOI
* Integrated with vegetation time-series

---

## Key Results

### 🌱 Vegetation Dynamics

* Seasonal NDVI and SAVI show strong dependence on monsoon rainfall
* Increased variability observed in the post-2014 period
* Threshold-based filtering highlights active vegetation zones

### 🌡️ Land Surface Temperature

* Gradual increase in LST over time, especially in urbanized regions
* MODIS and Landsat integration reveals long-term warming trends

### 🌧️ Rainfall Patterns

* High inter-annual variability in monsoon rainfall
* Strong correlation between rainfall peaks and vegetation response

---

## Sample Outputs

### NDVI Seasonal Trend

![NDVI Trend](outputs/ndvi_trend.png)

### SAVI Analysis

![SAVI Map](outputs/savi_map.png)

### LST Time Series

![LST Trend](outputs/lst_trend.png)

### Seasonal Rainfall

![Rainfall Chart](outputs/rainfall_chart.png)

---

## Repository Structure

```
├── NDVI/
├── SAVI/
├── LST/
├── CHIRPS/
├── outputs/
├── docs/
└── README.md
```

---

## Tools & Technologies

* Google Earth Engine (GEE)
* ArcGIS Pro / QGIS
* Python (GeoPandas, Rasterio, Matplotlib)
* PostGIS & Spatial SQL

---

## Applications

* Environmental monitoring
* Climate change analysis
* Urban expansion impact assessment
* Agricultural and vegetation studies
* Disaster and risk assessment

---

## Future Work

* Integration of LULC classification for change detection
* Machine learning-based vegetation prediction
* Higher temporal resolution climate–vegetation modeling

---

## Contact

**Akhil A**
Geospatial Engineer | Remote Sensing & GIS
📧 [anil.akhil021@gmail.com](mailto:anil.akhil021@gmail.com)
🔗 https://github.com/yourusername

---
