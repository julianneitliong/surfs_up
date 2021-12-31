# surfs_up
working with SQLite and Flask

## Overview of the analysis
### Purpose
The purpose of this analysis is to use data to make an informed business decision to see if opening a surf and ice cream shop in Oahu, Hawaii will be a good investment. Using temperature data, this analysis will show temperature data starting in 2010 for the months of June and December. 

### Results
When looking at the results of the June and December data, we can see these three major points:
* The average temperature for June is 75 degrees and the average temperature for December is 71 degrees
* The highest temperature it has gotten in June is 85 degrees and the lowest is 64 degrees
* The highest temperaure for December is 83 degrees and the lowest is 56 degrees

![jun](https://github.com/julianneitliong/surfs_up/blob/0dfa9acafd945894261ceab0e993eeceada0e251/june.png)
![dec](https://github.com/julianneitliong/surfs_up/blob/0dfa9acafd945894261ceab0e993eeceada0e251/dec.png)

### Summary
Looking at the two summary statistic dataframes for June and December temperatures, we can see there is not an extreme difference in the two months' average temperatures. Because of this low variance between the two months' average temperatures, customers will still be interested in purchasing ice cream in both the summer months and winter months. 

Two additional queries I would use is to look at the precipitation data for both of those months. Even though the average temperature for the two months stay consistent, understanding how much it rains may be helpful in predicting if there will be customers out surfing or interested in purchasing ice cream when it rains. 

### June Precipitation Data
june_rain = session.query(Measurement.date, Measurement.prcp).filter(extract("month", Measurement.date) == "6").all()

### Dec Precipitation Data
dec_rain = session.query(Measurement.date, Measurement.prcp).filter(extract("month", Measurement.date) == "12").all()
