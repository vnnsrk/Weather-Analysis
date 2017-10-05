# Weather-Analysis
We analyze the US climate data from NCDC with multiple statistical and machine learning methods, to identify patterns, trends and indicators for global temperature changes

## Dependencies
1. PySpark
2. FindSpark
3. Numpy & Scipy
4. gmplot

## Data

The data used for the analysis is hosted at this [link](https://drive.google.com/open?id=0B_Cz1ZeaITeDYUNXUk5udE5NYk0). The data should be downloaded and stored in the [Data](https://github.com/vnnsrk/Weather-Analysis/Data/) folder. Then do,

```
$unzip -f Data.zip
```

It was extracted from the NCDC website. It consists of climate statistics such as Mean temperature of the day, max and min temperatures, humidity etc of the weather stations in the given area, along with the latitude, longitude and timestamp of the recording. The full description of the dataset is available in the schema of the data.

## Example distribution of data
![Image Not Found](/Images/location_map.JPG?raw=true "Distribution of data")

## Cities of interest

The dataset was analyzed in 3 main, distinct and climatically diverse areas.

1. California
2. Montana
3. Florida

## Approach

1. Primarily the data was loaded, and the spatial span of the weather stations were analyzed.
2. A sanity check was done by comparing the data with other sources such as [US Climate data](https://www.usclimatedata.com/)
3. Then we plot the distributions of the mean and variance, the eigen values and the percentage of variance explained by the eigen values. This visual inspection helps us to identify the key indicators of change/variation.
4. We do an analysis of multiple climatically important factors like TOBS (Temperature observed), SNWD (Snow fall) etc. and identify their eigen coefficients. We try to reconstruct the variation by PCA and other dimensionality reduction techniques.
5. We identify the cummulative distributions and plot the data in *geo-map*. 
6. We construct heat-maps and correlation matrices to identify key factors that affect the global change.
7. We then identify the eigen variations across different stations and identify key patterns of correlation
8. We also perform temporal and spatial analysis of temperature, precipitation, humidity and snow-fall
9. We finally perform generalized linear regression analysis with the contributing factors against temperature and identify that the TOBS value has steadily increased over the past 100 years, indicating a increase in average temperature.

## Can we infer Global warming? Sneak-peek!
![Image Not Found](/Images/extra1.png?raw=true "Proof of global warming")
