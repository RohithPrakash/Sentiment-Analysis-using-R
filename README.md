# Sentiment Analysis using R
Sentiment Analysis using Tweets. The tweets (related to a topic/hashtag) used are no more than 7 days old. 

Click [here](https://sentysis.shinyapps.io/Sentysis/ "Sentysis") for demo.

## Prerequisites

### Install R
Select your nearest mirror from [here](https://cran.r-project.org/mirrors.html), download and install the pre-compiled distribution with respect to your OS.

### Create a Twitter Developer Account
* Create a twitter account, if you don't have one yet.
* Go to [Twitter Developer](https://developer.twitter.com/en/apply-for-access) and click on "Apply for a developer account".
* login with your twitter account if prompted.
* Select your Primary reason for using Twitter Developer Tools.
* Verify the Twitter Username details associated to the developer account.
* Fill all the data required about your organization.
* Describe your intended use of the Twitter API.
* Describe how you plan to use the Twitter API.
* Accept the Developer Agreement (After reading, obviously) and verify your email account.
* Your application is under review, and you will receive a notification with the result.

### Create a new app in Twitter Developer

* Go to [Twitter Developer Apps](https://developer.twitter.com/en/apps), login if prompted.
* Click on "create an app".
* Fill up all the required fields and submit.
* Once verified you will be granted the customer and access keys.

## How to use the code

Use any IDE or text editor of your interest.

Download and install the packages listed

* NLP
* twitteR
* syuzhet
* tm
* SnowballC
* stringi
* ROAuth
* base64enc
* tm
* ggplot2
* wordcloud

Use the Consumer API key, Consumer API secret key, Access token and Access token secret obtained from the app created on Twitter Developer for "Twitter Access Authentication".
```R
# Twitter Access Authentication

consumer_key <- 'Customer API key here'
consumer_secret <- 'Customer API secret key here'
access_token <- 'Access token here'
access_secret <- 'Access token secret here'
```

Choose the topic you'd like to analyse.
```R
# Fetch tweets

tweets <- searchTwitter("#topic", n=1000,lang = "en")
```
In the "Fetch tweets" cell, replace "topic" with the topic you chose, "n" or the number of tweets related to the topic to be downloaded is set to a 1000 and "lang" or language is set to "English". Parameters "n" and "lang" are changeable.

Run the cells to view the sentiment graph.
