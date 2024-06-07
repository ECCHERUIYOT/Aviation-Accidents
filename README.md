# DATA ANALYSIS ON AVIATION ACCIDENTS

## Overview
This data analysis project aims to provide insights into the lowest risk aircraft that the business can purchase for its new venture.

## Business Understanding
The company is expanding in to new industries to diversify its portfolio. They are interested in purchasing and operating airplanes for commercial and private enterprises, but do not know anything about the potential risks of aircraft. 
The purpose of this analysis is to determine which aircraft are the lowest risk for the company start the new business venture with.

## Data Understanding and Analysis

### Source of Data
The dataset is from the National Transportation Safety Board in Kaggle that includes aviation accident data from 1962 to 2023 about civil aviation accidents and selected incidents in the United States and international waters.

### Description of data
The data contains details of various civil aviation aircrafts accidents that occurred between 1962 to 2023.
The data consists of 88,889 rows representing different accidents that occurred and 31 columns which represent different variables including the make of the aircraft,model of the aircraft,number of injuries,number of fatal injuries,date of accident.

### Visualisation
Bar graphs to compare the injuries and accident rate with the aircraft make were plotted.

##### Creating a plot for the maximum values for the injuries,fatal and uninjured numbers.
Maximum_values =({'Column': ['Fatal Injuries','Serious Injuries','Minor Injuries','Uninjured'], 'Maximum Value': [Highest_fatal_injuries,Highest_serious_injuries,Highest_minor_injuries,Highest_uninjured]})
plt.bar(Maximum_values['Column'],Maximum_values['Maximum Value'],color =['Red','Blue','Orange','Green'])
##### Labeling the x and y axis
plt.xlabel('Categories')
plt.ylabel('Maximum Value')
##### Labeling the title
plt.title('Maximum Values in four categories on injuries')
plt.show()

##### Plotting a bar graph for the accident rate for the first 50 rows
plt.figure(figsize=(10,6))
plt.bar(low_risk_aircraft.index[:50], low_risk_aircraft['Accident_Rate'][:50])
##### Labeling the x and y axis
plt.xlabel('Make')
plt.ylabel('Accident Rate')
##### Rotating the x axix labels to avoid overlapping
plt.xticks(rotation=90)
##### Labeling the title
plt.title('Accident Rate per aircraft make')
plt.show()
plt.tight_layout()

##### Plotting a bar graph for the injury rate
plt.figure(figsize=(10,6))
plt.bar(risk.index[:50] ,risk['Injury_Rate'][:50])
##### Labeling the x and y axis
plt.xlabel('Make')
plt.ylabel('Injury Rate')
##### Rotating the x axis labels by 90 degrees to avoid overlapping
plt.xticks(rotation=90)
##### Labeling the title
plt.title('Injury Rate per aircraft make')
plt.show()

## CONCLUSIONS
From the analysis above;
1. Out of the 7588 different aircraft makes,5550 of them are considered low risk on accident rate and injury rate.
2. There were alot of null values which were replaced by 0
3. Aircraft make 'Boeing' had the highest serious injuries

## RECOMMENDATIONS
From the analysis;
The business has a big selection of aircrafts to choose from as more than half of the aircrafts in the dataset are considered low risk.
