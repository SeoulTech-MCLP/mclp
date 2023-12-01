# SEOUL TECH BA Subjects

## Problem Description
### Super Aged Society
Recently, the population of elders are increasing in Korea
### Insufficient amount of elder facilities
Not enough facilities that can cover most of elders
### Inappropriate location of elder facilities
Elder facilities are located at the place where elders can not approach easily

## Goal
Find optimal location of elder facilities that can cover elder population

## Data
### Elder population data 
Contains population of elders at each district
### Elder transported data 
Contains transported elder population at each district. Elder population destinated to certain district is recorded
### Elder living alone population data
Population of elders who live alone is recorded. The elders are separated into who are the subject of support, paid less, and the others who are not involved in these 2 categories 
### Elder facility data 
Number of elder facilities and each total amount of member acceptance
### Bus stop location data
### Subway location data

## Data EDA
Found out correlation with each variables

Since target variable will be demand of elder facility, we focused on features that are correlated to the target

Roughly, variables colored between orange and red are evaluated as high correlated

## Feature Engineering
Random Forest is an ensemble learning algorithm that is widely used for both classification and regression tasks

Using Random Forest, most important features for the target variable ‘Demand of elder facilities’ could be derived

Min-Max Scaling was held to prevent data that contains large value to dominate model
Results were shown as below

## Clustering
Good technique to find out the clusters of the data points with the similar value of x-axis and y-axis

To figure out which districts are categorized as showing high demand

Doing one clustering is not enough to select right cluster and its districts

Hence, 4 types of clustering method were used:
	1. K means clustering
	2. K medoids
	3. Hierarchical clustering
	4. Gaussian mixture

As a result, districts that are overlapped for all clustering methods will be selected as a target of MCLP technique

## MCLP

