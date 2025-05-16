# Reddit-Bot-News-Article-summarizer.-

Article Summarizer
This project implements a custom algorithm to extract the most important sentences and keywords from Spanish and English news articles.

It was fully developed in Python and it is inspired by similar projects seen on Reddit news subreddits that use the term frequency–inverse document frequency (tf–idf).

The 3 most important files are:

scraper.py : A Python script that performs web scraping on a given HTML source, it extracts the article title, date and body.

summary.py : A Python script that applies a custom algorithm to a string of text and extracts the top ranked sentences and words.

bot.py : A Reddit bot that checks a subreddit for its latest submissions. It manages a list of already processed

Reddit Bot
The bot is simple in nature, it uses the PRAW library which is very straightforward to use. The bot polls a subreddit every 10 minutes to get its latest submissions.

It first detects if the submission hasn't already been processed and then checks if the submission url is in the whitelist. This whitelist is currently curated by myself.

If the post and its url passes both checks then a process of web scraping is applied to the url, this is where things start getting interesting.

Before replying to the original submission it checks the percentage of the reduction achieved, if it's too low or too high it skips it and moves to the next submission.
