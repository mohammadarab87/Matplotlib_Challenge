# Matplotlib - The Power of Plots
### ***What good is data without a good plot to tell the story?***
![chemistry-lab-apparatuses-500x500](https://user-images.githubusercontent.com/113273722/212503847-884f90bb-a65c-45a1-b7b7-51555811f341.jpg)

## Background
This respository apply a Python Matplotlib to visualize a real-world pharmaceutical data. 
The data is sourced from Pymaceuticals Inc.
Pymaceuticals specializes in anti-cancer pharmaceuticals. Recently, 
it began screening for potential treatments for squamous cell carcinoma (SCC),a commonly occurring form of skin cancer.
***In this study*** :
249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured.

The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.
hese analysis used a complete data from their most recent animal study in two datasets in CSV format.

Dateset one is ***Mouse_metadata.csv***, wich includes 249 mice identified data with SCC tumor growth were treated through a variety of drug ***regimens***
and their ***Sex***, ***Age_months*** and ***Weight(g)*** 
The other dataset is ***Study_results.csv*** which includes the results of the study in each columns,
***Mouse ID***,***Timepoint***,***Tumor Volume (mm3)***, and ***Metastatic Sites***.

## Tasks
### 1- Prepare the data. 
- Merge the ***Mouse_metadata*** and ***Study_results*** DataFrames into a single DataFrame.
- Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points
- Creat a cleaned Data after remove any mouse ID with duplicate time points,this will be the new date for the remaining steps.

### 2-Generate summary statistics.
The summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen

### 3-Create bar charts and pie charts.
those charts crearted by using both methods: ***Pandas's DataFrame.plot()*** and ***Matplotlib's pyplot***

that show the total number of time points for all mice tested for each drug regimen throughout the study. 
### 4-Calculate quartiles, find outliers, and create a box plot.
Calculate the final tumor volume of each mouse across four of the most promising treatment regimens:
***Capomulin***, ***Ramicane***, ***Infubinol***, and ***Ceftamin***.

Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens

### 5-Create a line plot and a scatter plot.

A line plot shows the tumor volume vs. time point for one mouse treated with Capomulin

A scatter plot shows average tumor volume vs. mouse weight for the Capomulin regimen
### 6-Calculate correlation and regression
The correlation coefficient and linear regression model are calculated for mouse weight and average tumor volume for the Capomulin regimen
## Observable Trends
- The bar graph showed the Drug Regimen Capomulin has the maximum mice number (230)
and Zoniferol has the smaller mice number (182)
By removing duplicates the total number of mice is 248. The total count of mice by gender also showed that 124 female mice and 125 male mice.
- The correlation between mouse weight, and average tumor volume is 0.84. It is a strong positive correlation,
when the mouse weight increases the average tumor volume also increases.
- The regression analysis helped us to understand how much the average tumor volume (dependent variable) will change when weight of mice change(independent variables)
 The R-squared value is 0.70, which means 70% the model fit the data
 wich is fairely good to predict the data from the model. Higher R-squared values represent smaller differences between the observed data
 and the fitted value. 70% the model explains all of the variation in the response variable around its mean.
 - From the selected treatments Capomulin and Ramicane reduces the size of tumors better
