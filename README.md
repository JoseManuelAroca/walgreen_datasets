WALGREEN
=============================================
Soil organic carbon is a key indicator of soil health, fertility, and carbon sequestration, playing a central role in sustainable land management and climate change mitigation. In this article, we present WALGREEN, a cloud-based platform designed to enhance soil organic carbon estimation by integrating remote sensing data, machine learning methods within a Software-as-a-Service framework, and heterogeneous soil datasets. The platform leverages extensive soil observations, including publicly available datasets such as the Land Use/Cover Area Frame Survey (LUCAS) soil database, and focuses on prediction at the continental European scale. WALGREEN integrates scalable data-processing pipelines and machine learning workflows to automatically generate prediction models from multi-source geospatial data. It exploits Google Earth Engine to extract reflectance vectors from Sentinel-2 and Landsat-8 imagery and incorporates high-dimensional embeddings from AlphaEarth Foundations, alongside imagery from the Copernicus Program. Experimental results demonstrate strong predictive performance, with models trained on cropland samples (maize, barley, and wheat) achieving R² = 0.94 on LUCAS validation datasets.These results highlight the potential of combining remote sensing observations, foundation-model embeddings, and machine learning to improve estimation. WALGREEN supports researchers, policymakers, and land managers in analyzing soil organic carbon spatial patterns and informing soil and land management decisions at large scales.
<img width="1880" height="1052" alt="figure1 (1)" src="https://github.com/user-attachments/assets/44b1c8a9-3969-4428-a195-0fb85898ab14" />
Preprint submitted to Computers and Electronics in Agriculture March 27, 2026

**Table of contents**
* [Architecture](#architecture)
* [Features](#features)
* [Datasets](#datasets)
* [Papers](#papers)
* [License](#license)


### Architecture

<img width="1920" height="1080" alt="figure2 (1)" src="https://github.com/user-attachments/assets/8c7b8086-b444-4d59-b4dd-1d2b122912af" />

WALGREEN architecture is based on an MVC front-end and back-end coded in Java using Spring boot, Hibernate, and Spring data JPA with Thymeleaf. The Earth observation side is based on an API coded in Python using WSGI and flask.

Flask is a popular framework for developing minimal apps or often creating restful API. It is considered a micro-framework that provides only the essentials of a web framework without enforcing other components. WSGI (uWSGI), the master daemon that runs and supervises the Python worker processes, is responsible for time-capped requests, recycling workers, background tasks, cron jobs, timers, logging, auto reloads on code changes, and run-as privileges. 

Depending on the different features, API methods can invoke the Copernicus Data Space Ecosystem Sentinel HUB or Google Earth Engine API points to set up synchronous or asynchronous interactions to serve JSON format data structures when called from the back-end application side. API points can be divided into four categories: 
*  Google’s AlphaEarth Foundations API points: AlphaEarth Foundations is an advanced AI model that provides a consistent, compact summary of the planet’s terrestrial land and coastal waters, enabling high-precision global mapping and monitoring.
* Google Earth Engine API points: Google Earth Engine's (GEE) public data catalog includes a variety of standard Earth science raster datasets with remote sensing information. You can load these datasets into your script environment with a single click of a button. You can also upload your own raster or vector data for private use in your scripts. Earth Engine radar images from the Copernicus Program include rain or snow-free radar images from Sentinel-1A and 1B, as well as high-resolution optical images from Sentinel-2A and 2B are three examples of GEE integration.
* Copernicus Program API points: The Copernicus Data Space Ecosystem offers multiple Application Programming Interfaces (API points) ranging from catalog and product download to visualization and processing web services, such as STAC, openEO, and Sentinel HUB API points. WALGREEN is integrated with Sentinel HUB API points and allows users to access raw satellite data, rendered images, statistical analysis, and other features.
* Data Science & Machine Learning API points: WALGREEN offers, in SaaS mode, a set of predictive models based on ensemble methods. ML ensembles in scikit-learn  are methods that combine multiple base models to improve predictive performance and robustness compared to individual estimators. WALGREEN includes Bagging (Bagging Regressor \citep{breiman1996bagging}), which trains models on random subsets of data to reduce variance.

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

## Datasets
User can upload different type of files:
1. CSV file:
2. KML file: Is a Keyhole Markup Language (KML) file designed for geospatial visualization of Soil Organic Carbon (SOC) sampling points. This file enables the visualization of SOC field observations in GIS tools such as Google Earth, QGIS and    Web-based KML viewers.
It is primarily used to inspect spatial distribution and attributes of SOC measurements generated or processed within the WALGREEN platform.
The KML file contains:
 Screen Overlay
     Displays copyright information:
- Source: OpenStreetMap contributors
- License: CC-BY-SA 2.0
* Folder: POI
- Contains SOC sampling locations
* Subfolders (e.g., 1)
- Group points by category or dataset partition
* Styles
- style-cropland
- style-other
- Define marker appearance (blue circular icons)
2. Copernicus script file
## Papers

J. M. Aroca et al., "WALGREEN: Web Based Platform for Soil Organic Carbon Inference Applications," IGARSS 2024 - 2024 IEEE International Geoscience and Remote Sensing Symposium, Athens, Greece, 2024, pp. 3992-3996, doi: 10.1109/IGARSS53475.2024.10642525.
keywords: {Training;Water;Surveys;Visualization;Satellites;Soil measurements;Machine learning;Soil organic carbon;machine learning;datasets;Sentinel integration;Tiff and Geo Tiff;Spring boot Framework;Java Persistance API;Python API;Flask},

## Git Hub Repositories
 [tomimick/restpie3](https://github.com/tomimick/restpie3) -RESTPie3 - Python REST API Server Starter Kit


License
-------
MIT License

