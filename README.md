
# Surfs_Up

Weather Data Analysis (Hawaii)

## Analysis Purpose

In order to determine if the surf and ice cream shop business in Oahu, Hawaii is sustainable year-round, we were tasked to analyze temperatures for the months of June and December.



## Approach

•	Using ***extract*** function, we were able to parcel out the data for June and December

`june_tobs = session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date) == 6).all()`

`december_tobs = session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date) == 12).all()`

•	We then looked at the key metrics using .describe() method 

`df_jun.describe()`

•	Utilize visual tools to show trends



## Results

### *June*

•	Between 2010 and 2017, average June temperature was at 75F degrees with min temperature 64F and max 85F.

![]( https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/june_summary.PNG)



* We can also see frequency of the occuring tempeartures from the graph below, which shows us that out of 1700 days of record we have, less than 200 records (11%) was recorded at below 70F.


![](https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/jun_temp_occurence.png)


* June temepratures trend shows that 2015 was the coldest year.

![](https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/jun_temp_trend.png)


### *December*


•	December average temperature for the same period was 71F degrees with minimum 56F and max 83F.

![]( https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/december_summary.PNG)



* December temperature occurence 

![](https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/dec_temp_occurence.png)


* December temperature trend shows that 2014 was the coldest year.


![](https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/dec_temp_trend.png)



## Summary

Based on the available data for 2010-2017, we see that Hawaii’s temperature was quite “steady” all year -round. With June avg of 75F and 71F in December, ice cream busines seems to be a good investment. Of course, our data does not account for any force-major situations (like covid-19!) so this is just a high-level assumptions. If we look at June vs December temperatures, we see that Oahu is a wonderful place to invest in business.

![](https://github.com/jojobear2020/Surfs_Up/blob/master/analysis/jun_dec_temp_kdeplot.png)

# ALOHA! 
