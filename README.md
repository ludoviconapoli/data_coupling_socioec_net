# data_coupling_socioec_net
Tutorial notebook for the course Digital Data Collection Methods. Goal of the tutorial is to explain how to couple a communication dataset and socioeconomic map from the census to obtain a socioeconomic network.

The communication data is based on a portion of a real dataset, with multiple randomization and manipulation steps to ensure complete anonymization, so that only the link weights in the network have been preserved (otherwise it's completely synthetic): 
- users' IDs have been renamed randomly 
- date and time of communication have been randomized
- geolocation of towers has been synthetically centered around Paris and randomized

The data folder contains multiple files:

- BASE_TD_FILO_DISP_IRIS_2014.xls: this is an Excel file that gives us multiple SES indicators of geographical units called ISIS. In particular, we will use the Median Income indicator. From the website of the INSEE: "In order to prepare for the dissemination of the 1999 population census, INSEE developed a system for dividing the country into units of equal size, known as IRIS2000. In French, IRIS is an acronym of ‘aggregated units for statistical information’, and the 2000 refers to the target size of 2000 residents per basic unit". The dataset can be downloaded here: https://www.insee.fr/fr/statistiques/3288151/
- CONTOURS-IRIS_D075.shp: this is a standard shapefile with the shapes of the IRIS unit located in the Paris area. The IRIS shapefiles of all the French Départments can be found here: https://geoservices.ign.fr/documentation/diffusion/telechargement-donnees-libres.html#contoursiris
- CDR_sample.dat: sample of (anonymized, randomized) CDRs data. The entries are separated by a | symbol and are organized in this order:

date, in YYYYMMDD format
time, in HHMMSS format
caller ID
callee ID
cell tower ID
event type (call or SMS)

- towers_geolocation.txt: file containing the (shifted and randomized) geospatial coordinates of cell towers in this order (tab-separated):

tower_id  longitude latitude

- tour.png: figure of tour eiffel




