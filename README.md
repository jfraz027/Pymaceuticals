# Pymaceuticals
## Background

As a senior data analyst for Pymaceuticals Inc., which is a new pharmaceutical company specializing in anti-cancer pharmaceuticals which rececently, began screening potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. 

In my role at the company, I was given access to the complete data from the most recent animal study. In this study, 249 mice were identified with SCC tumor growth and treated with a variety of drug regimens. Over period of 45 days, tumor development was observed and measured. The purpose was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. 

The executive's also requested the development of the tables and figures required for the technical report icluding a top-level summary of the results.

## Work

Key tasks are the following:

* Prepare the data.

* Generate summary statistics.

* Create bar charts and pie charts.

* Calculate quartiles, find outliers, and create a box plot.

* Create a line plot and a scatter plot.

* Calculate correlation and regression. 

* Submit final analysis. 

Important steps were necessary for the development of the analysis.

## Data Preparation

    1. Run dependency and data imports, and then merge the DataFrames into a single DataFrame.
        - mouse_metadata
        - study_results
    2. Display the number of unique mice IDs in the data, checking for those with duplicate time points.
    3. Display the data associated with that mouse ID, create a new DataFrame with this data removed and then prepare clean     
       DataFrame for the remaining step.
    4. Display the updated number of unique mice IDs.

## Summary Statistics Generation

Create two summary statistics DataFrames:

     1. For Table 1, utilze "groupby" method to generate the mean,median,variance,standard deviation, and SEM for the tumor 
     volume for each drug regimen resulting in five unique series objects.Then combine objects into a single summary statistics 
     DataFrame.
     2. For Table 2, use the `agg` method to produce the same summary statistics table utilizing a single line of code.

## Bar Charts,Pie Charts Creation

     1. Generate two identical bar plots showing the total number of timepoints for all mice tested with each drug regimen. 
                * Create the first bar plot by using Pandas's `DataFrame.plot()` method.
                * Create the second bar plot by using Matplotlib's `pyplot` methods.

     2. Generate two identical pie plots showing the distribution of female or male mice.
                * Create the first pie plot by using both Pandas's `DataFrame.plot()`.
                * Create the second pie plot by using Matplotlib's `pyplot` methods.

![image](https://user-images.githubusercontent.com/99145651/163817321-a04a3da5-8887-4d61-9d64-9a11318f28da.png)

![image](https://user-images.githubusercontent.com/99145651/163817553-ffd6a8b9-1b2c-40e4-8d64-a506d75cea57.png)


## Quartiles Calculation, Outliers Discovery, Box Plot Creation 

     1. Calculate the final tumor volume of each mouse across treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. 
     Then, calculate the quartiles and IQR and determine whether there are any potential outliers across all four treatment 
     regimens which are considered the four most promising.
         Follow substeps:
         * Create a grouped DataFrame that shows the last (greatest) time point for each mouse and merge this with the original 
         cleaned DataFrame.
         * Create a list that holds the treatment names,and also a second, empty list to hold the tumor volume data.
         * Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each 
         treatment. Then append the resulting final tumor volumes for each drug to the empty list. 
         * Determine outliers by using the upper and lower bounds include print out of results.
    
      2. Using Matplotlib, generate a box plot of the final tumor volume for all four treatment regimens and highlight any 
         potential outliers in the plot by changing their color and style.

![image](https://user-images.githubusercontent.com/99145651/163817469-6df5625a-1e64-4064-a506-2f03c44e225e.png)


## Line Plot and a Scatter Plot Creation 
      
      1. Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.
      2. Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

## Correlation and Regression Calculation 

      1. Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for 
      the Capomulin treatment. 
      2. Plot the linear regression model on top of the previous scatter plot.


![image](https://user-images.githubusercontent.com/99145651/163816948-02167df8-2149-4824-9f6c-06215350e848.png)

![image](https://user-images.githubusercontent.com/99145651/163817687-b0cb309c-0c37-4941-ba6d-e0e4a83a8b3f.png)









