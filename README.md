# Udacity-Project-2
#Introduction
>The objective of this project is to perform wrangling, analysis and visualization on  tweet archive data of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dogs. 
>The tweet archive contains some basic tweet information which doesn’t allow for some insightful analysis and visualization to be made. Therefore some additional data will need to be gathered which are Image prediction  data and some basic tweet information which has been omitted from the tweet archive but can be collected via a twitter API.
>This report documents how I walked through the wrangling process.

#The Wrangling Process
>1.	Gathering Data
I gathered three (3) data set which were in different data format and from different sources.
a.	WeRateDogs: This was provided by Udacity as a download and was an csv file. I therefore downloaded data into my designated folder and read data into my jupyter notebook
b.	Image Prediction Data: This is hosted on Udacity’s servers and an URL was provided. I therefore used the request library to download this unto my computer, saved and read it into my jupyter notebook.
c.	Twitter API: Following the steps given on ‘How to Query Twitter Data’, I signed into my twitter account and set my developer account in order to have my consumer key & secret and access token & secret.
I followed the code captured in the ‘twitter_api.py’ file provided in the Udacity Classroom to query the additional data. However, I was unsuccessful with it. I therefore proceeded to use the resultant data i.e tweet_json.txt already provided in the Udacity Classroom by reading it programmatically into my notebook

2.	Assessing Data
I assessed all three (3) dataset visually and programmatical. Since the WeRateDogs data was csv, I was able to visually assess it in excel in addition to the visual assessment in the notebook. I assessed datasets for quality and tidiness issues.
a.	Quality Issues: Below are some of the quality issues I found
WeRateDogs
•	I required only original ratings not retweets and replies
•	There were missing values in the following columns; in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp and expanded_urls
•	There was inconsistency of entries under expanded_urls Columns
•	There was inaccurate/inconsistent entries for name column
•	Timestamp was a string data instead of datetime data
•	
Image Prediction
•	There was inconsistency in capitalisation of names under columns p1, p2 and p3
•	Some image predictions are not dog
•	There is duplication in jpg_url columns
•	There extreme values for rating_numerator and rating_denominator

Tweet_json Data
•	Extreme values for retweet_count and favorite_count confirmed

b.	Tidines Issues
WeRateDogs 
•	The following columns; doggo, floofer, pupper and puppo are categorical and can be under one column
•	The columns source and expanded_urls have complex observation units
The three (3) different data sets needs to be merged together since they are related to same observational unit
3.	Cleaning
I cleaned the data set by addressing almost all the issues I raised especially the ones that relevant to my analysis and visualization

After cleaning the data, I stored it into the specified file format and name i.e twitter_archive_master.csv

Conclusion 
I must indicate that though the cleaning stage is tedious, I have learnt a lot and it is interesting to be able to run a code that performs exactly what you want.
