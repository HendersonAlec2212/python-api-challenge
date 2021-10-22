# python-api-challenge

# Intro
The purpose of this project was to show how one could, using data analysis methods, answer the question:
>"Does it get hotter closer to the equator?"

# Data Set
The data set was made by requesting data through an API before being cleaned and set into a DataFrame. A slightly noteable limitaion with this data set would be any present limitaions associated with the API key and the time someone has to accumulate the data.

# Method
We started off by using generating a list of random Latitude and Longitude values before passing them through a library named citypy to verify what the closest city to the location values would be. Once we had a sufficient sample size of real, unique city names, it was time to make some API calls to [https://openweathermap.org/] and retrieve data concerning the most recent weather conditions. These conditions were stored in to a dataframe, cleaned to eliminate outliers, then set to be used as a source for scatter plot and linear regression data.
Now that the new database was ready for processing, it was time to graph. For ease and simplicity we defined a function for the initial scatter plots and a second function to serve as a scatter plot / linear regression combo. Afterwards, we produced a total of 12 graphs displaying a range of correlations between the location of the city and aspects of it's weather.

# Analysis
**Both Hemispheres**

When comparing the Hemispheres in one graph, it was easiest to spot a trend in the change of temperature as one approaches or moves away from the Equator. Other graphs varied widely in the dispersion of city-points and showed no visible correlation but to be sure the data was separated into Norther and Southern Hemispheres before being passed through a linear regression / scatter plot function for thorough examination of the math behind the data.

**Northern & Southern Hemisphere**

- _Max Temperature (F) & Latitude:_

At the top of the comparisons is the most successful correlation, that of Max Temperature (F)
& Latitude.
These plots had the highest R-Value of 0.743 and 0.568, respectively, the correlation of the data becomes more pronounced as the R-value approaches -1 or 1 so in these two situations, the values display that the y-axis was quite dependent on the x-axis.

No other graphs came close to providing an R-value suitable for mentioning which is exactly why we will discuss why that may be.
> Item vs Items (R-value: North, South)

- Humidity vs Latitude (0.0018, 0.065)
- Cloudiness vs Latitude(0.012, 0.077)
- Wind Speed vs vs Latitude(0.0918, 0.068)

These weather attributes change according to the distance from a large body of water and/or the amount of water vapour in the air, not as one approaches the Equator. Hence the strong correlation between the Temperature and Latitude.

### Potential issues with Linear Regression

- The coefficient of determination, r^2 works best to predict values when the relationship between variables is linear. If r is close to zero, the change in x-values will not be a good predictor of y, in general. So as the line is intended to predict values of y for values of x that are close to the data. Using the line far outside that range may produce unrealistic forecasts.


# Conclusion

Few graphs produced correlations as strong as that of the Latitude vs. Temperature figures, however it was interesting to see how many cities have an "all or nothing" trend when it comes to cloudiness. Seeing data of so many cities plotted before oneself, it is something to consider that the town I live in is quite bland with average temperatures, wind speeds, and humidities when compared to some the outlying cities in this generated data frame.

Graphing using Matplot is truly an artform and in practicing I learned so much more about parameters possible with line plots to make more dynamic scatter plots combining partially transparent points with a black outline to produce a shading effect.