# Project 3: Web APIs & Classification

### Guide to Documents in Folder

After general setup, the notebooks were split in two:
1. Intitial Analysis deals with understanding the base data set, including model scoring, calibration, and word clouds
2. Misc Subreddit Analysis points the subbreddit analyzer at a series of new subreddits

The Subfolders are as follows:
1. Workbook History - Previous versions (usually simpler and messier) used to arrive at conclusions
2. Presentation - Contains powerpoint brief and figures used to populate the brief 


#### General Discussion of Methodology

After the initial analysis, it became clear that the model had a baseline prediction of republican for most subreddits, even after introduction of the null set. Upon further investigation, it became apparent that there were many more high scoring dem words, penalized by a larger intercept. When loosing the model in the wild, it became clear that a systematic adjustment had to be made to the results. 

This problem was partially fixed by using countvectorizer instead of the original TF-ID, which incidentally had a higher upfront accuracy rate. Interestingly, Trump as a predictor word dissapeared from both the top of both lists when using countvectorizer. 

Utlimately, when predicting probabilities from logistic regression on each post, I opted to simulate setting the intercepts equal by bumping up the predicted proba for the dem score. This is done in the subreddit_analyzer function, but can be switched off for comparison. This produced much better variation in predictions. 

### Conclusion
Forcing a model to make predictions it is not intended to make is a mess, but possible. It produces some interesting results and I look forward to sniffing out further political types across the internet.
