The Project is present in Shared Drive, We are providing Access to you so you can remotely run it without need to install any dependencies.

If you want to run it locally then following are the steps:

1.Download Kafka and put the folder in the working directory i.e., folder name as per version "kafka_2.13-3.3.1"
2. Put the Historical Data File named "training.1600000.processed.noemoticon.csv" in the working directory

3. Install these packages: 
	kafka-python
	git+https://github.com/tweepy/tweepy.git
	pymongo
	pyspark py4j


There are 3 files, run them in mentioned order:
1. "Twitter Stream - Tweepy | Kafka | PySpark | MongoDB.ipynb"

   This file contains the following code:
	Gets the twitter stream using tweepy
	Stores the tweets stream in Kafka having "Facebook/Meta" related tweets
	Creates Streaming Data Frame from Kafka Consumer in Spark
	Conducts Text Processing & Sentiment Analysis of the Tweets
	Loads the Resultant Tweets in MongoDB

2. "Streaming Tweets Visualization.ipynb"

   This file contains the following code:
	Reads Data containing Streamed Twitter Sentiment Analysis Data Set from MongoDB
	Caps the Data to as many tweets as in Historical Data
	Creates Heat Map of Sentiments Classification Count
	Creates Pie Chart with Tweets Sentiment Count
	Creates Word Cloud in General, Positive, Negative, and Neutral Sentiments
	Calculates Aggregated Sentiment Score
	Screenshort of Tableau Dashboaard

3. "Historical Tweets Analysis.ipynb"
   
    This file contains code to:
	Reads Data from the "training.1600000.processed.noemoticon.csv" as Spark Data Frame
	Filters data to have only "Facebook" related tweets
	Conducts Text Processing & Sentiment Analysis of the Tweets
	Loads the Resultant Tweets in MongoDB (Will be Used in Tableau Viz)
	Reads the Data from MongoDB
	Creates Heat Map of Sentiments Classification Count
	Creates Pie Chart with Tweets Sentiment Count
	Creates Word Cloud in General, Positive, Negative, and Neutral Sentiments
	Calculates Aggregated Sentiment Score
	Screenshort of Tableau Dashboaard
	

Visualizations in Tableu (For Both Twitter Stream & Historical Data)

To Connect Tableau Dekstop to MongoDB
1. Install the Driver:  https://search.maven.org/artifact/org.mongodb/mongodb-jdbc
2. In MongoDB Atlas Cloud, Put the Collection in Data Federation
3. In Tableau, Connect to MongoDB Atlas, enter credentials
4. Once it is connected, go to sheets and created visualizations
5. The sheets visualizations can be then aggregated in Dashboard

The packaged Tableau Files are enclosed, named as:
HistoricalData-603.twbx
StreamedData-603.twbx
	

