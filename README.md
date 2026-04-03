WALGREEN
=============================================
Soil organic carbon is a key indicator of soil health, fertility, and carbon sequestration, playing a central role in sustainable land management and climate change mitigation. In this article, we present WALGREEN, a cloud-based platform designed to enhance soil organic carbon estimation by integrating remote sensing data, machine learning methods within a Software-as-a-Service framework, and heterogeneous soil datasets. The platform leverages extensive soil observations, including publicly available datasets such as the Land Use/Cover Area Frame Survey (LUCAS) soil database, and focuses on prediction at the continental European scale. WALGREEN integrates scalable data-processing pipelines and machine learning workflows to automatically generate prediction models from multi-source geospatial data. It exploits Google Earth Engine to extract reflectance vectors from Sentinel-2 and Landsat-8 imagery and incorporates high-dimensional embeddings from AlphaEarth Foundations, alongside imagery from the Copernicus Program. Experimental results demonstrate strong predictive performance, with models trained on cropland samples (maize, barley, and wheat) achieving R² = 0.94 on LUCAS validation datasets.These results highlight the potential of combining remote sensing observations, foundation-model embeddings, and machine learning to improve estimation. WALGREEN supports researchers, policymakers, and land managers in analyzing soil organic carbon spatial patterns and informing soil and land management decisions at large scales.

Preprint submitted to Computers and Electronics in Agriculture March 27, 2026

**Table of contents**
* [Architecture](#architecture)
* [Features](#features)
* [Papers](#papers)
* [License](#license)


### Architecture


### Features
🚀 Key Features<br/>
🌐 Google Earth Engine (GEE) integration<br/>
🛰️ Multi-sensor data fusion:<br/>
     Sentinel-2<br/>
     Landsat-8<br/>
🧠 AlphaEarth 64-dimensional embeddings<br/>
🤖 Automated ML pipelines using scikit-learn<br/>
🌲 Ensemble models (RF, GBM, ExtraTrees)<br/>
📍 Spatial prediction (lat/lon based)<br/>
⏳ Multi-year SOC modeling<br/>
📊 Auto-generated visualizations (scatter, residuals)<br/>

## Papers

J. M. Aroca et al., "WALGREEN: Web Based Platform for Soil Organic Carbon Inference Applications," IGARSS 2024 - 2024 IEEE International Geoscience and Remote Sensing Symposium, Athens, Greece, 2024, pp. 3992-3996, doi: 10.1109/IGARSS53475.2024.10642525.
keywords: {Training;Water;Surveys;Visualization;Satellites;Soil measurements;Machine learning;Soil organic carbon;machine learning;datasets;Sentinel integration;Tiff and Geo Tiff;Spring boot Framework;Java Persistance API;Python API;Flask},

## Git Hub Repositories
 [tomimick/restpie3](https://github.com/tomimick/restpie3) -RESTPie3 - Python REST API Server Starter Kit


License
-------
MIT License

