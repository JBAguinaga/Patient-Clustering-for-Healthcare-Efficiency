![UTA-DataScience-Logo](https://user-images.githubusercontent.com/98781538/226424191-8cadd40f-3610-4ed5-93b1-9e9072098975.png)


# Patient Clustering for Healthcare Efficiency

* **Summary**: This repository holds my attempt apply a clustering algorithm (K-means) to Hospital patient discharge data directly from New York's Statewide Planning and Research Cooperative System (SPARCS).

## Overview

  * **Definition of the tasks / challenge**: The task is to use a the N.Y. SPARCS discharge dataset, which contains detailed information on up to 34 patient attributes, as a base to apply a K-means clustering algorithm and provide "data discovery" to better identify groups or "clusters" within the dataset for better organization and clarity of the types of patients.
  * **My approach** The approach in this repository formulates the problem as a discovery task, comparing patient attributes, gathering relevant information and ultimately running a clustering algorithm on the dataset.
  * **Summary of the performance achieved**: N/A

## Summary of Workdone

### Data

* Data:
  * Type: 
    * Input: CSV file with Patient discharge attributes, specifically pertaining to health and patient condition (ie. Gender, Race, Diagnosis, Age group, Risk of mortality, etc. vs cost of charges, hospital county, facility ID, etc.)
  * Size: 930MB
  * Instances: 2.54 million instances for clustering w/ 34 attributes per individual

#### Preprocessing / Clean up
*  Multiple missing/null values for variety of attributes. I used Pandas to create dataframes, remove any null instances and ultimately clean the dataset.
*  Group of columns that were deemed irrelevant to project were dropped including 'Operating Certficiate Number', 'Payment Typology(s)', 'Facility ID', etc.
*  Attributes listed as "objects" instead of strings, integers, floats, etc. Used Pandas library to modify columns/attributes into appropriate form and then plotted values via histograms.

#### Data Visualization

![LengthofStay](https://user-images.githubusercontent.com/98781538/226444439-c157c899-ae50-4d28-9ee3-54003e7709ad.png)
* One of the most relevant metrics to determine where individuals are clustered into is the amount of time they spent in the hospital. Here, we observe the frequency of instances (y-axis) based on the amount of days stayed (x-days). For our dataset, the vast majority of individuals spent 20 days or less as patients. Only a marginal amount were beyond that.

![Plotbyage](https://user-images.githubusercontent.com/98781538/226447271-6ca52745-9133-41b4-b430-f0a6cb040633.png)
* This plot provides a summary of which age ranges had the highest frequency in our dataset. Not surprisingly, the frequency of hospitalization increased as age increased, starting from the age of 30 to 70 and upwards. The least hospitalized group (lowest frequency) was 18-29 years of age group. (Note: Group 0-17 has higher hospitaliztion than 18-29).



### Problem Formulation

* Defined:
  * Input: Patient Discharge Attributes, specifically pertaining to health and patient condition (ie. Gender, Race, Diagnosis, Age group, Risk of mortality, etc. VS. Cost of charges, hospital county, facility ID, etc.)
  * Output: Groupings of individual patient types
  * Models: N/A

### Performance Comparison

* N/A

### Conclusions

* N/A

### Future Work

* N/A

## How to reproduce results

* N/A

### Overview of files in repository

* Describe the directory structure, if any.
* List all relavent files and describe their role in the package.
* N/A

### Software Setup
* N/A

### Data

* Download link: https://health.data.ny.gov/api/views/u4ud-w55t/rows.csv?accessType=DOWNLOAD&bom=true&format=true
* CSV file will have attributes uploaded into Jupyter Notebook as "objects". Optional to change data type option on import and adjust values manually from there.
* Dropped multiple columns via DataFrame manipulation using Pandas functions.

### Training

* N/A

#### Performance Evaluation

* N/A


## Citations

* Previous Work: [A system for exploring big data: an iterative k-means
searchlight for outlier detection on open health data 
](https://github.com/JBAguinaga/ProjectTemplate/files/11022006/2018.K-means.Health.data.paper.pdf)

