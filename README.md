# Crime Patterns in Toronto (K-Prototypes and K-means Clustering)

### Introduction
The aim of this project is to combine crime data obtained from the Toronto Police Service (TPS) with Toronto based climate data from the Government of Canada to uncover patterns in criminal activity in the city as it relates to climate. Cluster analysis is employed to group the data such that objects in the same cluster share more similar properties than objects in other clusters.

- Each record in the preprocessed dataset represents a unique occurrence, including details of the crime committed and temperature/climate on the day of the occurrence.
- Substantial data cleansing and preprocessing was required to transform the raw data into a format suitable for clustering analysis.
- The k-prototypes algorithm from the kmodes package is used to handle the mix of categorical and numerical features in the preprocessed dataset. 
- The more popular k-means algorithm is also employed after some additional preprocessing, however the more versatile k-protoypes algorithm yielded more insightful information due to its ability to handle catagorical data.
- The k-prototypes algorithm was able to locate 5 meaningful clusters. Each record was then assigned to one of these clusters.
- Data visualization and the aggregation of records by cluster was used to understand the charateristics of each cluster. 
- Code: [Link](https://github.com/calvinchoi21/toronto-crime-clustering/blob/master/Toronto_Crime.ipynb)

### Contents

<ol>
  <li>Data Preparation and Cleaning</li>
  <li>Data Exploration</li>
  <li>Application of K-Means Algorithm</li>
  <li>Application of K-Prototypes Algorithm</li>
</ol> 

### The Data
The final prepared dataset contains 15 features. Each record represents a specific occurrence. 

<ul>
  <li>event_unique_id - ID used to identify each occurrence</li>
  <li>offence - Name of offence committed</li>
  <li>occurrenceyear - Year of occurrence</li>
  <li>occurrencemonth - Month of occurrence</li>
  <li>occurrenceday - Day of month of occurrence</li>
  <li>occurrencedayofweek - Day of week of occurrrence</li>
  <li>occurrencehour - Hour of day of occurrrence</li>  
  <li>MCI - Crime category of offence</li>
  <li>Neighbourhood - Name of Toronto neighbourhood</li>
  <li>Date/Time - Data and time of occurrence</li>
  <li>mean_temp - Mean temperature on the day of occurrence</li>
  <li>total_rain - Total rain in CM on the day of occurrence</li>
  <li>total_snow - Total snow in CM on the day of occurrence</li>
  <li>total_precip - Total precipitation on the day of occurrence</li>
  <li>snow_on_ground - Total snow on ground on the day of occurrence</li>
</ul>  

The first ten features were obtained from the TPS <a href="http://data.torontopolice.on.ca/pages/catalogue">Public Safety Data Portal</a>. The last five features were obtained from the <a href="https://climate.weather.gc.ca/historical_data/search_historic_data_e.html#">Environment and Natural Resources</a> section of the Government of Canada website. 
