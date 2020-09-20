
# Surfs_Up

Weather Data Analysis (Hawaii)

## Analysis Purpose

In order to determine if the surf and ice cream shop business in Oahu, Hawaii is sustainable year-round, we were tasked to analyze temperatures for the months of June and December.


## Approach

•	Using ***extract*** function, we were able to parcel out the data for June and December
‘ december_tobs = session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date) == 12).all()’
•	We then looked at the key metrics using .describe() method
‘df_jun.describe()’
•	Utilize visual tools to show trends


## Results

•	Between 2010 and 2017, average June temperature was at 74.95 (F) degrees

![]( https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/june_summary.PNG)




•	December average temperature for the same period was 71.04 (F) degrees

![]( https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/december_summary.PNG)

## Summary

Based on the available data for 2010-2017, we see that Hawaii’s temperature was quite “steady” all year -round. With June avg of 75F and 71F in December, ice cream busines seems to be a good investment. Of course, our data does not account for any force-major situations (like covid-19!) so this is just a high-level assumptions. If we look at June vs December temperatures, we see that Oahu is a wonderful place to invest in business

![](https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/jun_dec_temp_kdeplot.png)

#ALOHA! 
