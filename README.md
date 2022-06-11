# surfs_up
## Project Overview

Overview of the analysis: Explain the purpose of the new analysis.
W. Avy is opening a shop in Hawaii. In order to have a successful launch and sustainable company, this analysis will help us understand weather / temperature trends before opening up shop for surfing and ice cream. 

## Resources
- Data Source: hawaii.sqlite database
- Software: Python, Pandas, SQLAlchemy

## Results
Results: Provide a bulleted list with three major points from the two analysis deliverables. Use images as support where needed.
* The average temperature in June is 74.9 with the highest temp on the record at 85. 
* The average temperature in December is 71.0 with the lowest temp on the record at 56. 
* The lowest temperature in June on the record is 64 and the highest temperature in December on the record is 83. <br>


**June Summary Table**
![June Summary Table](https://github.com/jinnabelle/surfs_up/blob/main/juneDF.png)

**December Summary Table**
![December Summary Table](https://github.com/jinnabelle/surfs_up/blob/main/decemberDF.png)

## Summary
Summary: Provide a high-level summary of the results and two additional queries that you would perform to gather more weather data for June and December.
Based on the results from the analysis above, I would recommend W. Avy to open up the surf and ice cream shop in Hawaii because these products are necessary throughout the whole year. The temperatures on average for these two months are relatively safe for both surfing and eating ice cream. The lowest temperature on record in December of 56 degrees might be worth calling out but according to the average, it does not get that low in temperature that often.

For further investigation, I would suggest looking at temperatures for a range of months for the summer and winter. I feel like this would give them a better understanding of the temperature for each seasons vs. one month. 
    session.query(Measurement.date, Measurement.tobs).filter(extract('month',Measurement.date).in_((6,7,8,12,1,2)))

I would also query precipitation in the winter months because I think rain has a big factor in people's decision of going out to surf and/or eat ice cream during the winter months. 
    session.query(Measurement.date, Measurement.prcp).filter(extract('month',Measurement.date).in_((12,1,2))).all()
