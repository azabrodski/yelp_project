"Do Friends on Yelp Give Similar Overall Ratings?"
========================================================
author: A Zabrodski
date: November 18, 2015
autosize: true

## Predicting the average rating of a users friends ##

The Question
========================================================

Yelp is a social network for reviewing businesses. Users access the website or use an app on their mobile phone to post reviews about their experience at a business. Other users can read these reviews which will help guide their choice about where to go for tacos or which dentist is the best in their local area. More information is available on the [Yelp](www.yelp.com) website. As of the second quarter of 2015, Yelp had a monthly average of 83 million unique visitors who visited Yelp via their mobile device and written more than 83 million reviews.

The purpose of this analysis is to look for predictive factors to estimate the average business rating of a users friends on Yelp. That is to say, do users who give high overall ratings also have a group of friends who give higher ratings. To be far more cynical, the question can be phrased as "Are jerks also friends with other jerks?" 

Methodology
========================================================

The question in it's most basic form asks if there is a relationship between a users average star rating and there friends. In order to keep the results interpretable we will start with a simple linear regression and analysis between a users rating and that of their friends. Secondly, we will expand the analysis to other measurable factors in the data such as if the user has given many compliments, or has received many votes that they had a "funny" or "cool" review. 

Using linear regression allows for very interpretable coefficients, as each coefficient quantifies the level of influence from each factor and it can be tested for significance. This is preferable to a random forest model which although may be very accurate, it is not easily interpreted.

Analysis
========================================================

<img src="Yelp Deck-figure/unnamed-chunk-1-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />

Results
========================================================

From the plot, there does appear to be some linear relationship between a users average rating (x-axis) and the average rating of their friends (y-axis). However, the linear regression models resulted in a coefficient of ~0.05 for a users average rating with an R^2 value of 0.09. So less than 10% of the variance can be explained by the users rating, and a full unit increase in rating (which is a lot on a 1-5 scale) would only result in 0.05 increase in their friends average rating. 

This analysis suggests that users on Yelp have a diverse mix of friends with a range of business rating behaviours, and that there is no relationship between a users average rating and that of their friends. 
