# Python_portfolio_project
I have worked on portfolio project given by atomcamp bootcamp. The title of the project is "Flight Delays and Cancellations Dataset". There were some question provided which i was supposed to answer them. 

To work on the project i have installed anaconda ( you can download anaconda from the link : https://www.anaconda.com/download), open jupytor notebook, where i have uploaded the data sets and imported the necessary libraries. analysize data sets and then answers step forward to answer the questions.

### Below are the question which i have answered and also visualized using python jyptor notebook and the thier related libraries:

Question: Which airline had the highest percentage of delayed or cancelled flights in 2015?
Question: Which airports had the most flight cancellations?
Question: Are there any geographical patterns in flight delays? Do certain regions or airports experience more delays than others?
Question: What was the average flight delay for each day of the week? Are weekends or weekdays more prone to delays?

### Project name = Flight Delays and Cancellations Dataset

-Datasets used: airlines, airports, and flights.
Importing libraries
import pandas as pd
import numpy as np
import matplotlib as plt
from matplotlib import pyplot

-Load data sets
After studying the content of the df, I decided to set the format of some of
the columns while importing the data in order to avoid DtypeWarnings
# Load data sets
airlines_df = pd.read_csv(r'D:\Mehran\porfolio projects\P.Project.D_Analysis_Python
airports_df = pd.read_csv(r'D:\Mehran\porfolio projects\P.Project.D_Analysis_Python
flights_df = pd.read_csv(r'D:\Mehran\porfolio projects\P.Project.D_Analysis_Python\
Analyzing the data sets
# Get the shape of each dataframe to get an idea about the number of instances we a
print("shape of airlines:", airlines_df.shape)
print("shape of airports_df:", airports_df.shape)
print("shape of flights_df:", flights_df.shape)
shape of airlines: (14, 2)
shape of airports_df: (322, 7)
shape of flights_df: (5819079, 31)
As it can be seen, the first dataframe has just 14 rows and two columns while the second
dataframe has 322 rows and 7 columns and the third has over 5.8 million rows and 31
columns.

# Now going through the information of the dataframes, so that
we can get some general insights about them.
airlines_df.info()
airports_df.info()
flights_df.info()
airlines_df.describe()
# checking duplicates
airlines_df[airlines_df.duplicated()]
airports_df[airports_df.duplicated()]
flights_df[flights_df.duplicated()] 

# Checking missing values
airlines_df.isnull().sum()
null_values2=airports_df.isnull().sum()
print("Null values:")
print(null_values2)
flights_df.isnull().sum()

# Answering to quentions:
###  Q1: Which airline had the highest percentage of delayed or cancelled flights in 2015?
Methodology:
Filtering flights data for the year 2015. Calculating total delayed or cancelled
flights per airline. Calculating total flights per airline. Determining percentage of delayed or
cancelled flights per airline.
