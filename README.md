# Rainfall Frequency Analysis (RainFA) package <img src="src/logo.png" align="right" width="200" />

## Description

RainFA develops a methodology for data curation and frequency analysis of rainfall series, programmed in Python, that allows: (1) homogenization of the temporal step; (2) performing data quality control; (3) determining homogeneous regions using the L-moments method from a prior process of clusters supported by the Silhouette width and Mantel statistics, as well as Ward's dendogram; and (4) calculation of the l-moments candidates for homogeneous regions according to the Discordancy and Heterogeneity measures. 

Further work will focus on extending the methodology to improve the geospatial and temporal distribution of precipitation in homogeneous regions by incorporating new tools into the RainFA gallery.

## How does it work

### Inputs

* Station data (.csv): a single file including for each station the following data: station ID, station name, WGS84 coordinates (Latitude, Longitude, Elevation). 
* Precipitation time series (.csv): a different file for each gauge station including station ID, date-time and instantaneous rainfall in (IR) mm.

### Calculations

Firstly, data curation and trend testing will help to depurate the rainfall time series.

* Precipitation time-series database (.parquet): Database with the homogeneized time-step date-time and instantaneous rainfall in mm.
* Boxplot graphs (.ipynb): Jupyter notebook for the calculation and graphical representation of single station boxplots.
* Double-mass graphs (.ipynb): Jupyter notebook for the calculation and graphical representation of single station double-mass graphs against average rainfall data.
* Mann-Kendall test (.ipynb): Jupyter notebook for the calculation of the Mann-Kendall trend test and associated statistics to determine the data stationarity.

Next, the following graphs will allow for cluster classification. For this purpose, the station data file is suplemented with two rainfall statistics summarised from the recipitation time series data file - i.e. annual rainfall and number of days with rainfall above 0.2 mm.  

* Mantel graphs (.ipynb): Jupyter notebook for the calculation and graphical representation of Mantel graph clustering method.
* Silhouette widths graphs (.ipynb): Jupyter notebook for the calculation and graphical representation of Silhouette widths graph clustering method.
* Ward's dendogram graph (.ipynb): Jupyter notebook for the calculation and graphical representation of Ward's dendogram graph.

Finally, l-moments ratios will allow the homogeneity of a region to be identified:

* L-moments discordancy measure (.ipynb): Jupyter notebook for the calculation of the Discordancy measure with l-moments.
* L-moments heterogeneicy measure (.ipynb): Jupyter notebook for the calculation of the Heterogeneity measure with l-moments.

## Case study

The package contains the necessary information to reproduce an example of the different subroutines in a hypothetical region of Spain.

## Authors

- [@Pablo Blanco-Gómez](https://orcid.org/0000-0001-9465-2912)
- [@Juan I. Ortiz-Vallespi](https://orcid.org/0009-0002-2317-740X)
- [@Pau Estrany-Planas](https://orcid.org/0009-0003-6665-5966)
- [@Javier Orihuela-Martínez](https://orcid.org/0009-0008-7602-0346)

## Acknowledgments

Authors acknowledge Vicente M. Candela Canales for supporting the R&D investment and programs within the Vielca companies.
