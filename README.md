# KNIME Workflows
Hydro KNIME
--------------------
Solar KNIME workflows
---------------------
Solar radiation modeling with KNIME. Increasing environmental model reproducibility and warantability by using scientific workflows

For all workflows users are required to install a freely available and open source KNIME Scientific Workflows Management System. KNIME can be downloaded from the following link: https://www.knime.com/downloads/download-knime.

User manual: Minimal Knime Workflow for Solar Analyst 
------------------
Required input data:

1) Parameter setting values (csv format file);
2) Digital Surface Model (DSM in ASCII format);and 
3) Geographic latitude for the study area. 

The main output: 
Table with solar radiation data for each raster cell (point) of the DSM

Dependencies: 

1) ESRI Solar Analyst integrated via python script. To integrate ESRI ArcGIS to workflow environment please use Anaconda environment. The steps to do this is provided on the following link: https://gisday.wordpress.com/2016/07/18/setting-up-anaconda-pysal-with-arcgis-python-environment/ ; and 
2) Input data needs to be in csv and ASCII file formats. 

Note: Workflows can be executed only on computer machines with Microsoft operating system because the ESRI ArcGIS installation is only available for Windows. 

User manual: Extended KNIME workflow integrating Solar Analyst wioth validation 
------

Required input data:

1) Parameter setting values (csv format file);
2) Digital Surface Model (DSM), a local path to ASCII file format); 
3) Geographic latitude for the study area; and
4) Ground truth solar radiation including tolerance for error difference (csv file format).

The main output: 
Table with solar radiation data for each raster cell (point) of the DSM and classified Solar Analyst outputs in three categories "Low", "Expected", and "High". 

Dependencies: 

1) ESRI Solar Analyst integrated via python script. To integrate ESRI ArcGIS to workflow environment please use Anaconda environment. The steps to do this is provided on the following link: https://gisday.wordpress.com/2016/07/18/setting-up-anaconda-pysal-with-arcgis-python-environment/ ; and 
2) Input data needs to be in csv and ASCII file formats. 

Note: Workflows can be executed only on computer machines with Microsoft operating system because the ESRI ArcGIS installation is only available for Windows. 

User manual: Workflow to expose solar radiation model details
--------------------------------------------------------------------------------------------------------------------------
Required input data:

1) XYZ coordinates for points of interest (txt file format); 
2) XYZ coordinates for all points from Digital Surface Model (DSM)(txt file format);
3) Local time in hours (csv file format); and 
4) Days of year (starting first day with 1.... 365 (csv file format).

Workflow flow variables: 
Global varaibles:
Latitude (Geographic latitude for the area of the interest, positive values for the North hemisphere and negative values for the South hemisphere). 
Local variables: 
1) Solar constant; 
2) Longitude (Geographic longitude for the area of the interest);
3) LSTM (Local standard time meridian;and
4) Azimuth sectors;

How to create and use variables please see the video on the following link: 
https://www.knime.com/knime-introductory-course/chapter7/section1/creation-and-usage-of-flow-variables

The main output: 
Table with solar radiation potential for all points of interest (input data(1)) togethere with their coordinates 

Dependencies:
1) R program language needs to be ran in background of local machine in order to execute R snippet nodes; and
2) Input data needs to be in txt and csv file formats.  

Workflows operates on Microsoft, Mac and Linux operative systems. 

User manual: Workflow for machine learning parameter-setting assistance
------------------------------------------------------------------------------------------------------------------------------

Required input data:

1) Parameter setting values (csv file format);
2) Geographic latitude (double value) and DSM (ASCII format) of the area of interest; and
3) Ground truth solar radiaiton data (csv file format).

The main output data: decision tree diagram.

Dependencies:

1) ESRI Solar Analyst integrated via python script. To integrate ESRI ArcGIS to workflow environment please use Anaconda environment. The steps to do this is provided on the following link: https://gisday.wordpress.com/2016/07/18/setting-up-anaconda-pysal-with-arcgis-python-environment/ ;
2) R program language needs to be ran in background of local machine in order to execute R snippet nodes; and
2) Input data needs to be in txt and csv file formats.  

Note: Workflows can be executed only on computer machines with Microsoft operating system because the ESRI ArcGIS installation is only available for Windows. 
