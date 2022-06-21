# PySpark Transformation Analysis on Amazon Tweets


## DATA DESCRIPTION
This dataset consists of 400,000+ tweets on Twitter, where users had contacted (@AmazonHelp) to give a review on amazon's service. 
The dataset includes several columns of data that can be analyzed:
* id_str: string id
* tweet_created_at: the date the tweet was created
* user_screen_name: the screen name of the twitter user
* user_id_str: user string id
* user_statuses_count: amount each user has of tweets
* user_favourites_count: amount of favourites each user has
* user_protected: TRUE or FALSE values for whether twitter user has a private account
* user_listed_count: count of user listed amount
* user_following: whether twitter user was following the @AmazonHelp account
* user_description: Bio of Twitter User
* user_location: location of Twitter User
* user_verified: TRUE or FALSE values for whether twitter user is verified or not
* user_followers_count: amount of followers each user has
* user_friends_count: amount of friends each user has
* user_created_at: when the twitter user account was created
* tweet_language: what language the tweet is in
* text_: content of the tweet sent
* favorite_count: amount of favorites on the tweet
* favorited: TRUE or FALSE values whether the tweet had been favorited
* in_reply_to_screen_name: screen name of the account that was replied to
* in_reply_to_status_id_str: string id value of account that was replied to
* in_reply_to_user_id_str: string user id value of account that was replied to
* retweet_count: number of amount of times the tweet was retweeted
* retweeted: TRUE or FALSE values whether the tweet was retweeted
* text: content of the tweet sent

## Goals
**1.**
Filtering only the Twitter users that are verified. For the verified users, grouping by created date, and counting the number of tweets for each date. With the date with the highest number of tweets, calculating the sum of favorite_count and retweet_count for each tweet on that day

**2.**
Using the find_text.csv. The csv consists of two columns: "id_str" and "text" with the "text" column empty. Finding out the text content of each tweet according to "id_str" while joining Amazon_Tweets.csv and filling in the "text" column


## RESULTS
Running the code on a 2021 M1 Pro, Python 3.9.13, and Spark version 3.2.1, the following code completed in 31.81 seconds on initial run. Running the code again, finished in 11:06  seconds. This shows the advantage of using Spark for huge datasets like this. I might re-create the above code to pandas and seeing how long it takes to run without a spark session as a test
