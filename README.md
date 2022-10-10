# Wrangle and Analyze Data 

The main aim of this project is to wrangle data to produce high-quality 
and tidy data which will eventually be analyzed to produce at least 3 insights and 1 visualization. 
The data will be gathered from 3 different sources in different formats: **csv, tsv, and txt**. 


## Installation 

``` 
import pandas as pd 
import numpy as np 
import requests 
import tweepy 
from tweepy import OAuthHandler
import json 
import matplotlib.pyplot as plt 
%matplotlib inline 
import seaborn as sns
sns.set_style("darkgrid")
```


## Gathering Data 

The data used in this analysis include:<br>
• Data from the tweet archive of Twitter user @dog_rates (or WeRateDogs) 
contained in a file on hand, `twitter_archive_enhanced.csv`, provided on Udacity.

• Data downloaded from the internet and stored in a file named 
`image_predictions.tsv`.

• JSON data for each tweet ID in `twitter_archive_enhanced.csv` 
downloaded from Twitter through Twitter API, using Tweepy library, 
and stored in a file named `tweet-json.txt`. 


## Datasets

The tweet data from the tweet archive of Twitter user @dog_rates (or 
WeRateDogs) has a total of 2356 rows and 17 columns, 
and consist of features such as the tweet ID, retweet observations (retweeted_status_id, 
retweeted_status_user_id, and retweeted_timestamp), 
the rating for each dog (rating_numerator and rating_denominator), and dog stages 
(doggo, puppo, pupper, and floofer) amongst others. The dataset can be found [here](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/59a4e958_twitter-archive-enhanced/twitter-archive-enhanced.csv) 

The data downloaded from the internet include features 
such as three image predictions (p1, p2, and p3) 
along with the confidence of the predictions (p1_conf, p2_conf, p3_conf), 
and features which returned True/False if each prediction was for a dog (p1_dog, p2_dog, p3_dog). 
It also includes the tweet IDs, image URLs, and the image number 
corresponding to the most confident prediction, 
and has a total of 2075 rows and 12 columns. 
It can be found [here](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv) 

Features in the JSON data obtained 
through Twitter API includes the tweet IDs from 
the WeRateDogs Twitter archive, along with the retweet 
and favorite (likes) counts for each of the tweet IDs. 
It has a total of 2327 rows and 3 columns.

The individual datasets will be cleaned and 
merged into a single dataset 
`twitter_archive_master.csv`.


## Summary of Findings

The analysis of the resulting clean master dataset showed that doggos 
receive higher ratings than puppers.  Also, dogs with high ratings generally receive more likes than those with low ratings, 
and lastly, Labrador retrievers get the most retweets. 

