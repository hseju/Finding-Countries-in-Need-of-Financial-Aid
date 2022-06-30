# Clustering the Countries by using Unsupervised Learning for HELP International

## Objective:
To categorise the countries using socio-economic and health factors that determine the overall development of the country.

## About organization:
HELP International is an international humanitarian NGO that is committed to fighting poverty and providing the people of backward countries with basic amenities and relief during the time of disasters and natural calamities.

## Problem Statement:
HELP International have been able to raise around $ 10 million. Now the CEO of the NGO needs to decide how to use this money strategically and effectively. So, CEO has to make decision to choose the countries that are in the direst need of aid. Hence, my Job as a Data scientist is to categorise the countries using some socio-economic and health factors that determine the overall development of the country. Then I need to suggest the countries which the CEO needs to focus on the most.

The Data has been taken from [Kaggle](https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data?select=Country-data.csv). 

## Approach
- Data Cleaning/ Data Wrangling
- Exploratory Data Analysis
- Building Model
- Model Evaluation

<hr>

## Overview:

Two main clustering algorithms were used to determine the clusters of country in dire need of financial aid. 

1. SBDCAN 

To find the best value of epsilon, Nearest Neighbors method was used with cluster value of 4. 

![image](https://user-images.githubusercontent.com/89634505/176596227-59e9cb69-ee50-439f-9c86-eb16e594f66a.png)


In this algorithm, with epsilon of 1.24 and min_samples of 3 as hyperparameters, the silhouette score was found to be maximum at 0.13554. This clustered the data into 4 main categories and outliers. The Blue color indicates -1 class which is for the outliers. United States and other few countries were categorized as outliers which suggests not very efficient clustering. 

![image](https://user-images.githubusercontent.com/89634505/176596501-090a243a-2613-4a8c-93a2-9c19b6987051.png)


2. K Means Clustering

For K means Clustering, n_clusters where taken as 5 and it provided the silhouette score of 0.3 which was maximum for a range of n value from 2 to 11. 

![image](https://user-images.githubusercontent.com/89634505/176596840-04b0180f-ebc8-4b8b-9804-2831123fdacc.png)

K Means clustering categorized the countires very well into 5 clusters compared to DBSCAN's 4 clusters and outliers. With 5 clusters, the class names were provided as below:

![image](https://user-images.githubusercontent.com/89634505/176597093-2511468f-b43d-4e07-a9dd-df8353089d3b.png)

Countires plotted on a map according to classification:

![image](https://user-images.githubusercontent.com/89634505/176597220-261f4628-714c-4485-af27-47a2992e0c01.png)

A Polar chart that will compare the average values of socio-economic factors for each class.

![image](https://user-images.githubusercontent.com/89634505/176597134-e3e0ecf8-3b5a-4b4f-9994-6767e7030be1.png)


Finally, here is a list of countires that require utmost attention in terms of financial needs. 

Afghanistan,
Angola,
Benin,
Botswana,
Burkina Faso,
Burundi,
Cameroon,
Central African Republic,
Chad,
Comoros,
Congo, Dem. Rep.,
Congo, Rep.,
Cote d'Ivoire,
Equatorial Guinea,
Eritrea,
Gabon,
Gambia,
Ghana,
Guinea,
Guinea-Bissau,
Haiti,
Iraq,
Kenya,
Kiribati,
Lao,
Lesotho,
Liberia,
Madagascar,
Malawi,
Mali,
Mauritania,
Mongolia,
Mozambique,
Myanmar,
Namibia,
Niger,
Nigeria,
Pakistan,
Rwanda,
Senegal,
Sierra Leone,
Solomon Islands,
South Africa,
Sudan,
Tanzania,
Timor-Leste,
Togo,
Uganda,
Venezuela,
Yemen,
Zambia


