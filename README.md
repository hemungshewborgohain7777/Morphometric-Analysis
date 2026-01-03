# 🏞 Morphometric Analysis of a Part of Sarbhang Khola Chhu River Basin

## 🔹 Project Overview / Problem Statement
Morphometric analysis is a quantitative evaluation of drainage basin characteristics that helps in understanding basin geometry, drainage behaviour, surface runoff, and erosion processes.  
This project focuses on analyzing the **morphometric characteristics of a part of the Sarbhang Khola Chhu River basin** using DEM-based hydrological tools in GIS. The study aims to extract drainage networks and basin features to understand flow behaviour and watershed structure.

---

## 🎯 Objectives
- To delineate the watershed and drainage network of the Sarbhang Khola Chhu River basin  
- To analyze flow direction, flow accumulation, and channel networks  
- To understand basin morphology and drainage characteristics using GIS-based hydrological modeling  

---

## 📍 Study Area
The study area covers a **part of the Sarbhang Khola Chhu River basin**, characterized by elongated basin geometry and varying elevation.  
The region exhibits well-developed drainage networks influenced by topography and slope conditions.

📌 *Refer to the map showing basin boundary and channel networks.*

---

## 🗂 Data Sources
- **Digital Elevation Model (DEM)**  
  SRTM DEM (30 m resolution)  
  https://earthexplorer.usgs.gov/

- **Boundary / Basin Mask**  
  Derived from DEM using hydrological tools

---

## 🛠 Tools & Methods

### Software Used
- ArcGIS 10.8
- Spatial Analyst tools or ArcHydroTools
- Excel for Morphological Analysis Calculations

## 🛠 Tools & Methodology

### Software Used
- ArcMap (Hydro Toolbox Extension)
- Spatial Analyst Tools (Enabled)
- Microsoft Excel (for morphometric calculations)

---

### Methodology: Morphometric Analysis & Watershed Delineation (ArcMap – Hydro Toolbox)

The morphometric analysis and watershed delineation were carried out using **ArcMap with the Hydro Toolbox extension**. The workflow involves DEM preprocessing followed by hydrological terrain analysis to extract drainage networks and catchment characteristics.

#### Steps

1. Download the **Area of Concern (AOC) DEM** from USGS Earth Explorer.  
2. Add the **Hydro Toolbox** in ArcMap (Note: this is an extension and not available by default).  
3. Ensure **Spatial Analyst Tools** are enabled.  
4. Navigate to **Terrain Pre-processing** in the Hydro Toolbox.  
5. Apply **Fill Sinks**  
   - Path: Spatial Analyst → Arc Toolbox → Fill  
   - Purpose: Remove depressions and correct DEM errors.  
6. Run **Flow Direction** from Terrain Pre-processing.  
7. Run **Flow Accumulation** to identify drainage paths.  
8. Execute **Stream Definition** to define stream cells using threshold values.  
9. Perform **Stream Segmentation** to segment stream networks.  
10. Run **Catchment Grid Delineation** to generate catchment grids.  
11. Apply **Catchment Polygon Processing**  
    - Converts catchment grids into polygon features.  
12. Execute **Drainage Line Processing** to generate vector drainage lines.  
13. Run **Adjoint Catchment Processing** to merge adjacent catchments.  
14. Use **Polygon Delineation** from Hydro Toolbox  
    - Select the bottom of a stream order to delineate the watershed polygon.  
    - Save the output as *Watershed* (or desired name).  
15. Clip drainage lines using the watershed boundary  
    - Geoprocessing → Clip  
    - Input Feature: Drainage Line  
    - Clip Feature: Watershed Polygon  

---

### Coordinate System Conversion
- Conversion performed from **Geographic Coordinate System (GCS)** to **Projected Coordinate System (PCS)**.  
- **From:** WGS 1984 (GCS)  
- **To:** PCS UTM Zone 45N – WGS 1984  

This conversion is required for accurate **length, area, and statistical calculations**.

---

### Stream Ordering & Length Calculation
- Stream orders were assigned by adding a new field **`order`** in the attribute table.  
- Stream lengths were calculated using the **Field Calculator** and converted to **kilometers**.

---

### Morphometric Parameter Calculation
Morphometric analysis was carried out using the extracted drainage and basin data. Calculations were performed in **Microsoft Excel** using standard morphometric formulas.

#### Parameters Calculated
- Linear Aspect  
- Stream Order  
- Stream Length  
- Number of Streams  
- Stream Length Ratio  
- Basin Perimeter  
- Bifurcation Ratio  
- Basin Length  
- Basin Area  
- Drainage Density  
- Stream Frequency  
- Drainage Texture  
- Watershed Area  

---

## 🗺 Key Outputs
- Filled Sink DEM  
- Flow Direction Map  
- Flow Accumulation Map  
- Catchment Classification Map  
- Channel Network & Basin Map  

---

## 📊 Results & Interpretation
- The flow accumulation map highlights **major drainage paths** and potential stream locations.
- Channel networks show a **hierarchical drainage system**, indicating natural surface runoff patterns.
- Catchment analysis reveals **spatial variation in drainage contribution** across the basin.
- The elongated basin shape suggests **moderate runoff response** during rainfall events.

---

## 📘 What I Learned
- Practical application of **hydrological modeling in GIS**
- Importance of DEM preprocessing, especially **sink filling**
- Extraction and interpretation of drainage networks
- Visual representation of morphometric parameters

---

## 🔮 Future Improvements
- Calculation of quantitative morphometric parameters (e.g., drainage density, bifurcation ratio)
- Integration of rainfall and land-use data
- Flood susceptibility or erosion risk analysis
- Validation using high-resolution DEM or field data

---


