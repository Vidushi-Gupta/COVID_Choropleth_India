# COVID-19 Visualization using Choropleth Maps (India, Maharashtra)

An exploratory data analysis on the COVID-19 data for India (state wise analysis) and Maharashtra (district wise analysis). The analysis presented here aims to present the spatial distribution and spread of the COVID-19 over time in India. In addition, the analysis further attempts to elicit linkages between high COVID-19 prevalence states and their economic contribution to the nation.

## Methods of Data Analysis

The analysis was conducted in Python language(version 2.7.16) using the Pandas, Numpy, Matplotlib, Seaborn and Geopandas libraries.

## Spatial Trend Analysis
To analyze the trend in the spread of the virus, a state-wise daily cases dataset was imported from https://api.covid19india.org/ . From the dataset, the confirmed COVID cases were considered for each state and then a time resampling was performed with regards to ‘M’. Time series resampling was performed on the dataframe to convert it from a daily to a monthly dataframe. Following this it was merged with a shapefile of India and the Matplotlib library was used in order to plot a choropleth map for the month of March, April and May.

Another spatial analysis was conducted for the state of Maharashtra wherein district wise confirmed, active, recovered and the deceased dataset was acquired from https://api.covid19india.org/. Using Matplotlib library, a choropleth map was plotted on a shapefile of Maharashtra for all these categories for all the cases reported until mid-June. 

### Visualization
![India](https://github.com/Vidushi-Gupta/COVID_Choropleth_India/blob/master/Maps/india%20choropleth%20maps.png)

With regards to the scale, the colour towards the shade of purple shows a higher prevalence of COVID (i.e. higher number of confirmed cases) in a particular state. As observed in the trends, the states of Maharashtra, Tamil Nadu and Delhi have been the worst affected cumulatively over the span of three months.

![Maha](https://github.com/Vidushi-Gupta/COVID_Choropleth_India/blob/master/Maps/maharashtra%20choropleth%20maps.png)

The following maps make it evident that the virus has been most prevalent in Mumbai and adjoining districts, with the other districts being less affected than the hotspot.

## Comparison:Prevalence to economic contribution
For the comparative analysis of the prevalence of COVID-19 and the economic contribution, I took into consideration the RBI dataset which provides the net value added (in Rs. crore) by each state into the national economy for the year 2017–2018.

### Visualization
![compare](https://github.com/Vidushi-Gupta/COVID_Choropleth_India/blob/master/Maps/comparison.png)

The red colour line shows the confirmed COVID-19 cases in each state with its corresponding scale in red on the right-hand side.
The bar plot is a measure of the economic contribution for each state with its corresponding scale on the left-hand side.


## Limitations
1.The data for the state of Ladakh was merged with the data of Jammu and Kashmir due to the absence of the geometry of Ladakh in the shapefile.
2.The RBI dataset for the Net State Value Added shows the values for the year of 2017–2018. The latest dataset wasn’t considered because of the greater number of missing values.
3.The data for the district of Palghar in Maharashtra was merged into the Thane district due to the absence of geometry of Palghar in the shapefile.
4.The greyish extensions in the maps are due to some coordinates missing in the shapefile used in the analysis.


## Conclusions
Through this exploratory data analysis, the following inferences have been derived. the prevalence of COVID has increased in various clusters in states of Maharashtra, Tamil Nadu and Delhi being highly affected.
The greater the economic activities undertaken in a state, the greater the number of COVID-19 positive cases. Higher economic activity also means a higher population and a much more developed area which would mean more testing resulting in higher confirmed cases count.
The qualitative reasoning to the following inference would be that a greater economic activity means a greater inflow and outflow of migrants both domestic and international. Since travelling and contact with infected (asymptomatic or symptomatic) carriers are the major cause of the spread of the virus, thus, it validates the above findings.


You can also review this [Blog](https://medium.com/@vidushig2020/covid-19-in-india-trends-and-determinants-fcd2cee5e9fc?source=friends_link&sk=5af89977d41bda58896cf57d39248c5a) for an in-depth analysis of this visualization. 

You're most welcome to use the notebooks and the datasets attached here or to fork the repository.

Happy Visualizing!
