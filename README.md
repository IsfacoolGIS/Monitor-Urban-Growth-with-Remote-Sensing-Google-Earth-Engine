# Monitor-Urban-Growth-with-Remote-Sensing-Google-Earth-Engine

✔✔ Urban Expansion Analysis Using Landsat Data (1990-2025)

Monitor Urban Growth with Remote Sensing & Google Earth Engine
This repository provides a fully automated workflow for monitoring urban expansion using Landsat data (1990-2025) in Google Earth Engine (GEE). The script utilizes advanced remote sensing indices, SAR-based analysis, and machine learning techniques to map and analyze urbanization trends.

🚀 Key Features & Innovations
🛰️ Multi-Sensor Landsat Integration
Dynamically processes Landsat 4, 5, 7 (TM/ETM+) and Landsat 8, 9 (OLI) to ensure consistency across different time periods.

Applies sensor-specific band renaming to avoid variable mismatches.

🌥️ Advanced Cloud Masking
Implements Landsat Collection 2 Level-2 Surface Reflectance (SR) cloud masking using QA_PIXEL bitwise operations.

Ensures high-quality images for urban analysis.

🏙️ Urban Expansion Mapping
Calculates multiple built-up indices for improved classification:
✅ NDBI (Normalized Difference Built-up Index)
✅ MNDWI (Modified Normalized Difference Water Index)
✅ BSI (Bare Soil Index)
✅ DBSI (Dry Built-up and Soil Index)
✅ SAVI (Soil Adjusted Vegetation Index)
✅ EVI (Enhanced Vegetation Index)
✅ CI, SI, RI, BI (Colorimetric Indices for land cover analysis)

Implements a bare soil mask to differentiate urban areas from naturally exposed soil.

🔥 Time-Series Urban Trend Analysis
Urban area extraction for each time period using index thresholds.

Generates urban expansion layers (1990-2025) and visualizes them in a color-coded time-series map.

Uses linear regression (trend analysis) to highlight urbanization patterns.

🎨 Dynamic Visualization & Legend
Implements a customized color palette for each year of urban expansion.

Adds an interactive legend to the GEE map UI.

Generates a title overlay for better presentation.

🔧 How to Use
1️⃣ Open Google Earth Engine (GEE)
Go to Google Earth Engine Code Editor.

2️⃣ Copy & Paste the Script
Clone this repository or copy the script into the GEE JavaScript editor.

3️⃣ Define Your Region of Interest (ROI)
Modify the roi variable to your area of study.

Example (New York City):

javascript
Copy
Edit
var roi = ee.Geometry.Polygon([
  [-74.2591, 40.4774], [-73.7004, 40.4774],
  [-73.7004, 40.9176], [-74.2591, 40.9176]
]);
4️⃣ Run the Code & Visualize
Execute the script and explore urban expansion from 1990 to 2025.

🖼️ Output Layers
Layer Name	Description
Built-up 1990 - 2025	Color-coded built-up area for each year
Urban Trend	Linear trend analysis showing expansion hotspots
🏆 Why This is Unique?
✅ Uses multiple built-up indices instead of a single one (e.g., NDBI-only approaches).
✅ Integrates all Landsat generations seamlessly.
✅ Excludes bare soil areas for more accurate built-up detection.
✅ Automates urban trend analysis over 35 years.
✅ Can be applied to any city worldwide with minimal modifications.

📜 License
This project is released under the MIT License. Feel free to modify and improve it!

👨‍💻 Author: Ishfaqul Haque
📩 Contact: ishfaqulhaque1@gmail.com

🔗 Next Steps
✅ Improve accuracy using SAR-based built-up mapping.

✅ Integrate AI/ML models (Random Forest, SVM) for classification.

✅ Compare results with Night-Time Lights (VIIRS/DMSP) data.

🔥 Star this repo ⭐ if you find it useful! Fork and contribute to improve urban mapping with GEE! 🚀

![](https://github.com/IsfacoolGIS/Monitor-Urban-Growth-with-Remote-Sensing-Google-Earth-Engine/blob/b8f73373c918a9c96a64d89e7abc4639edcbbbc7/Screenshot%20(173).png)
