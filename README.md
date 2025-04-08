
![imengine prod srp navigacloud](https://github.com/user-attachments/assets/779ae46d-06ed-44f2-b562-ad0407258045)


# <ins>Monitoring The Los Angeles Wildfires in Early 2025</ins>

This project focuses on utilizing Earth Engine data to monitor and visualize wildfire activity in **Los Angeles, USA** in **January 2025**. The project authenticates with Earth Engine, initializes it with a specific Project ID, and sets up an interactive map centered on a user-defined region of interest (ROI) in Los Angeles.

The core of the analysis involves accessing and processing three key datasets from the **VIIRS (Visible Infrared Imaging Radiometer Suite)** sensor:
1. _VNP09GA_ (**VIIRS Surface Reflectance Daily 500m and 1km**): This dataset is used to calculate the Normalized Difference Vegetation Index (NDVI). NDVI is a crucial indicator of vegetation health and can highlight areas with stressed or burned vegetation, potentially indicating fire impact. The script filters this dataset for the specified time period (_January 1-February 1, 2025_), selects the necessary bands (_l1 and l2_), calculates the _NDVI_, and converts the resulting image collection into an _XArray_ dataset for easier analysis and plotting. The script then generates a time-series plot of the _NDVI) across the _ROI_.
2. _VNP14A1.002_ (**Thermal Anomalies/Fire Daily L3 Global 1km SIN Grid**): This dataset directly provides information on thermal anomalies and fire activity. The script filters it for the same time period, selects the _'MaxFRP'_ (_Maximum Fire Radiative Power_) band, and converts it into an _XArray_ dataset. A time-series plot of the maximum fire radiative power is then generated to visualize temperature variations potentially associated with fires.
3. _VNP21A1D.002_ (**Day Land Surface Temperature and Emissivity Daily 1km**): This dataset provides daily land surface temperature (LST) data. The script filters it for the specified period, selects the _'LST_1KM'_ band, and converts it to an _XArray_ dataset. A time-series plot of the land surface temperature is created to further visualize temperature patterns in the region.

In summary, the project leverages **Earth Engine** and the **VIIRS** sensor to analyze _surface reflectance (for NDVI)_, _thermal anomalies/fire information_, and _land surface temperature_ data to monitor and visualize wildfire events and their impacts in the Los Angeles area in January 2025. The use of _XArray_ facilitates the temporal and spatial analysis and visualization of these geospatial datasets. The output includes plots of _NDVI_ and temperature variations over time within LA.
