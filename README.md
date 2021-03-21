# PyBer_Analysis
mod 5

# Overview of the analysis: Explain the purpose of the new analysis. #
  The point of this analysis is to better present the Pyber driver date  y combining the two csv files of ride data and city data into a single readable file.
  `
  pyber_data_df = pd.merge(ride_data_df, city_data_df, how="left", on=["city", "city"])
  `
This allowed us to further breakdown the data into a readable chart.
```# 8. Using the object-oriented interface method, plot the resample DataFrame using the df.plot() function. 

ax = week_fares_by_date.plot(figsize=(20, 7.5))

# Add the title,  label and grid.
ax.set_title('Total Fares By City Type')
ax.set_ylabel('Fare ($USD)')
ax.set_xlabel ('Month')



ax.set_yticks(np.arange(0, 2550, step=500.0))
ax.grid(True)
ax.legend(('Rural','Suburban','Urben'), fontsize="12", mode="Expanded",
         scatterpoints=1, loc="center", title="City Type")


# Import the style from Matplotlib.
from matplotlib import style
# Use the graph style fivethirtyeight.
style.use('fivethirtyeight')

# Save plot to analysis folder
plt.savefig("analysis/pyber_challenge.png")```

With this chart we can easily show usage trends broken down by users geographic location.

  # Results: Using images from the summary DataFrame and multiple-line chart, describe the differences in ride-sharing data among the different city types #
 ![alt text]( https://github.com/sheepesq/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary..png)
![alt text]
