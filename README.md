# PyBer_Analysis
mod 5

# Overview of the analysis: Explain the purpose of the new analysis. #
  The point of this analysis is to better present the Pyber driver date  y combining the two csv files of ride data and city data into a single readable file.
  ```
  pyber_data_df = pd.merge(ride_data_df, city_data_df, how="left", on=["city", "city"])
  ```
This allowed us to further breakdown the data into a readable chart.
```ax = week_fares_by_date.plot(figsize=(20, 7.5))

# Add the title,  label and grid.
ax.set_title('Total Fares By City Type')
ax.set_ylabel('Fare ($USD)')
ax.set_xlabel ('Month')

ax.set_yticks(np.arange(0, 2550, step=500.0))
ax.grid(True)
ax.legend(('Rural','Suburban','Urben'), fontsize="12", mode="Expanded",
         scatterpoints=1, loc="center", title="City Type")
         
 ```

With this chart we can easily show usage trends broken down by users geographic location.

  # Results: Using images from the summary DataFrame and multiple-line chart, describe the differences in ride-sharing data among the different city types #
 ![alt text]( https://github.com/sheepesq/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary..png)

  As you can see in the chart above, as population density goes down the amount of ride fares also goes down. 
  
  # Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types. #
  - The first recomndation is that you can increase advertising in the rural and suburban area to increase usage of your service.
  - Encourage drivers to service rual and suburban areas as those locations have significantly less drivers than the urban areas.
  - You can increase the fee in urban areas to increase total profit as the avg fee in urban areas is less than rural or suburban.

