---
layout: page
title: Trump and the COVID19 Infodemic
subtitle: Adadakadavra Team
---

<div class="title-background">
    <img src="assets/img/title.jpg" style="display: block; margin: 0 auto; width: 100%;"/>
</div>
&nbsp;

# Context

Remember the beginning of 2020? The Covid pandemic suddently broke out. The disease was unkwnon, not understood
and scary. Most of the countries decided to lock down to stop the spread of the virus and protect their populations. This resulted in
major and global changepoints in mobility, as measured by Apple and Google's mobility data :

<div class="mobility-report">
    <img src="assets/img/mobility.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

We can spot two distinct patterns here, distinguishing between weekdays and weekends.
On weekdays, a majority of businesses either had to close or transition to telecommuting. This impact persisted beyond
the lockdown period, as indicated by the data.
Conversely, weekends also experienced disruption, but this effect diminished to near pre-restriction levels after the
restrictions were lifted.
We are particularly interested in studying this second part, as during the weekend, people were not working and had free
time to engage in various activities.

This time at home was ideal for cooking, watching cat videos (or playing with your cats) and spending time on the internet.
Interestingly, the global internet traffic followed the mobility evolutions:

<div class="mobility-report">
    <img src="assets/img/wikipedia_usage.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

Notably, while the time spent at home witnessed a more significant increase on weekdays, the surge in web searches,
estimated with the number of Wikipedia searches, was more pronounced during weekends. This is expected, considering that
weekdays were still occupied by telecommuting activities.

A linear regression analysis supports this observation. When regressing the number of web searches against the time
spent at home, the weekends exhibit a substantially higher coefficient of 2.52, in contrast to the coefficient of 0.84
observed during the week.

The evolution of the main topics searched for online during the pandemic has already been studied, e.g. by [Manoel et al.](https://arxiv.org/abs/2005.08505) . But internet traffic during Covid was
not only about cooking recipes and cats: it was also a great time to propagate fake news, what the [WHO](https://www.who.int/health-topics/infodemic#tab=tab_1) called an infodemic. The predecessor of X, Twitter, was one of the biggest place to propagate information, especially in quickly changing times such as the Covid pandemic. We all know that not all people have the same voice
on Twitter, and few of them can be considered to be among the most influential individuals on the network. If you had to bet on a
person to be particularly influential on Twitter, who would it be?

**Take a few seconds and answer to yourself, who would it be?**

I don't know who you had in mind, but for us, it had to be Donald Trump. Before he was evicted from the network (Jan, 9
2021), he was
one of the most followed account (81 millions followers in 2020). If you don't remind his tweets' style, here is a
refresher :

<div class="internet">
    <img src="assets/img/trump_sample_tweet.png" style="display: block; margin: 0 auto; width: 45%;"/>
</div>

We all know Donald Trump spread fake news, especially on Twitter, his favorite communication channel. His tweets
during the Covid pandemic spread like wildfire, probably making him one of the most influential figures during the
pandemic – but in the end, was he that influential? Will causal analyses of the effect of Trump’s tweets on Wikipedia
and Google Trends pageviews show that he was leading or following online trends? Our goal is to study the impact an
influential leader can have on information spread in a crisis with a focus on fake news, as an overload of misleading or
contradictory statements are known to have a detrimental impact on crisis management.

### Anatomy of "The Donald" Twitter Account

Now we want to know a little bit better the main character of this datastory. For this purpose, we will analyze his
tweets. One could argue that it is impossible to understand a person just by looking at what he tweeted, the sample is just
too small. Well, it's certainly not the case for our protagonist!

<div class="internet">
    <img src="assets/img/trump_tweets_michi1.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

As you can see it seems like Trump was always tweeting!
The numbers are just too good to be true. In the period we are considering, the year 2020, he
tweeted/retweeted every day, with a mean of more than 33 tweets per day and peaks of as much as 150 tweets/retweets in
one single day. Assuming he spent 16 hours per day awake means that on average he posted one tweet/retweet every half
an hour every day for an entire year. The good news are not even finished yet, he is not just speaking by himself, but he
reaches millions of people. This is shown by the millions of likes (almost 2 millions a day on average) and
thousands of retweets (more than 600 hundred thousands a day on average) that his posts boast.

Now taht we know that there is enough material to work with, let's try to understand the character. In order to know him
better, we want to see what he is most interested about. We extrapolated this information visualizing his most used words.

<div class="internet">
    <img src="assets/img/world_cloud_michi2.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

We can see that most of his favorites words are related to his continuous political campaigns. We notice the words "
vote", "election", "WhiteHouse", but also many regarding his opponent Joe Biden and the former's political faction: the
Democrats. You can also see his favourite disrespectful nickname for Biden: "Sleepy Joe".
One thing is certain: you can understand quite a lot about a person just by looking at their tweets when they tweet 30 times a day!
In fact, if you look closely, much more interesting words for our analysis, like "Coronavirus", "China" and "Fake News", also appear.
Let's filter the tweets using some keywords related to Covid to see if something interesting appears.

<div class="internet">
    <img src="assets/img/retweets_covid_michi5.png" style="display: block; margin: 0 auto; width: 100%;"/>
</div>

With no surprise the "hottest" period for covid-related tweets is the one at the start of the pandemic, in March 2020. It was not
only the period in which Trump tweeted the most about Covid, but it was also the period in which his Covid-
related tweets were most successful among his followers, being the most retweeted ones. But what are the most used words in Covid-
related tweets?

<div class="internet">
    <img src="assets/img/world_cloud_covid_michi3.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

Of course, when filtering with Covid as a keyword, it becomes the most popular item. But some interesting words like "
swine flu" and "china virus" also start popping up, and "fake news" becomes much more important. We thought that this
shifting in the topics was also due to Trump's tendency to reporting news from unreliable sources, such as those that claimed
the virus was due to a bad management of the swine flu during Obama's mandate. This was totally
unrelated to Covid, but Trump used it as a scapegoat for his own poor management of the pandemic.

We asked ourselves if, using a Latent Dirichlet Allocation, we would be able to isolate a cluster of tweets with these
interesting topics without having to manually select the fake-news related ones. We chose as a reference period the one 
stretching from early March to late May: as we saw earlier, most Covid-related online activity happened in this time.

{% include grafico_lda.html %}

Playing around a little bit with the graphical interface, we see that the algorithm selects these three main topic
clusters:

<div class="internet">
    <img src="assets/img/topic_clusters_michi6.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

Given the non-informative nature of these clusters we draw the conclusion that there is Donald Trump's
tweets mainly tend to be related to his political campaigns, even when they mention Covid. A huge part of his political campaigning is centered
around talking about the other political faction, rather than the urgent problems of the nation. For this reason, an automatic
algorithm does not fit very well the purpose of identifying tweets related to fake news. Instead, we chose to select them manually.


## Trump the Trend Maker or Trump the Follower, that is the Question!

Next, let's dive into the meat of our problem, with one of our main research questions: is there a causal relationship between Trump's tweets and the number
of visits on some Covid-related topics, e.g. hydroxychloroquine on Wikipedia? During the COVID-19 period, Trump claimed that hydroxychloroquine was a cure for COVID-19. 
This claim was not supported by scientific evidence, however, making it more of a fake news really. 
This was further motivation to investigate this topic in particular: Trump, an actor of the infodemic or not? Let's find out!

### Evolution of Online Trends and Trump's Tweeting: a first Graphical Inspection

To answer our question, let's start by graphically studying the evolution of the number of queries/visits on the topic of hydroxychloroquine to assess whether
Trump's tweets had an impact on them.

<div class="internet">
    <img src="assets/img/hydro_wiki_timeseries_daily.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

As we can see from the graph above, Trump's tweets on hydroxychloroquine seem to precede certain attention
peaks (e.g. the second big peak at the start of April), but come after others (e.g. the first big peak, around
mid-March). But then, do tweets cause views or the other way around?

### Granger Causality - Do Trump's Tweets give useful Information for Predicting Online Interest?

Clearly, a visual inspection of the evolution of tweeting and daily Wikipedia views makes it difficult to assess whether Trump causes tweets or the other way around.
To further investigate the causal relationship between tweeting and online public interest, we therefore chose to conduct
a [Granger causality](https://en.wikipedia.org/wiki/Granger_causality) test. "The Granger causality test is a statistical hypothesis test for 
determining whether one time series is useful in forecasting another". The [null hypothesis](https://www.statsmodels.org/dev/generated/statsmodels.tsa.stattools.grangercausalitytests.html)
is that "the the time series the first column is NOT Granger caused by the time series in the other columns".

We conducted two Granger causality tests: "Trump's Granger causes views on Wikipedia" and "Views on Wikipedia Granger
cause Trump's tweets". 
Both Granger causality tests are statistically significant at the 5 % threshold: Trump's tweets Granger cause 
Wikipedia views and vice versa.

How to interpret the fact that the two time series Granger cause each other? As mentioned earlier, Granger causality
just means that one time series is useful at predicting the other. It doesn't necessarily imply real causality.
 There can therefore be two explanations to our results:
 
- sometimes Trump causes tweets, other times public interest causes Trump to tweet;
- or both time series are actually caused by external factors. Sometimes Trump's reacts faster, and sometimes the public
  get interested first. The varying reaction times could explain the Granger causality results.

### Causal Impact - A tool to assess the Impact of one of Trump's Tweets on Online Trends

To further investigate whether Trump's tweets cause views, we will focus on his first tweet, which coincides with a big
peak in interest (both on Wikipedia and Google).
The [Causal Impact](https://google.github.io/CausalImpact/CausalImpact.html) library in Python allows us perform a test
to study the causal effect of Trump's first tweet on the number of Google queries on hydroxychloroquine.
We are focusing on Google Trends queries, as they allows us to study time series at hourly granularity, unlike Wikipedia.
To run this analysis we need the following variables:

- y: the number of visits to the the page of hydroxychloroquine (test variable).
- x: the number of visits to a set of pages (the control variables), which were not affected by the intervention (
  Trump's first tweet).

For the control variables, we picked the time series of the following five topics, which for obvious reasons should not have been affected
by Trump's tweet: climate, coffee, news, shop and time. 

A causal impact analysis for this first tweet corroborates the visual inspection of the Wikipedia time series: the
peak in interest on hydroxychloroquine preceded Trump's first tweet. His tweet therefore didn't seem to have had a strong impact
on interest. Note, however, that we used global trends time series. It might be that Trump had a local impact (though probably not
strong) on Google searches, e.g. in the United States.

As explained earlier, an alternative possibility to explain why online trends time series and Trump's tweets Granger
cause each other is that an external factor is the "real" cause of the surge of interest.

Some online research revealed that the big peak in interest mid-March might have caused by the two following major
events, which both took place on March 16, 2020:

- A mobility changepoint in the United States following restrictions, according
  to [Manoel et al.](https://arxiv.org/abs/2005.08505),
- "A study on the use of hydroxychloroquine in patients with SARS-CoV-2 was published (online via Youtube) - The
  preliminary data from
  this small study was heard round the world", as quoted
  from [Saag et al.](https://jamanetwork.com/journals/jama/fullarticle/2772921).

We therefore tried to reconduct a causal impact analysis, considering March 16, 5 P.M. (GMT, so between 9 A.M and 12
A.M. in the USA) as our intervention time. The resulting plot can be seen in the following Figure.

<div class="internet">
    <img src="assets/img/causal_plot.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

The causal impact analysis shows that the intervention on March 16 (the mobility restrictions, the publication or both -
perhaps even other events: this period was quite hectic) had a strong impact on Google Trends searches.

In conclusion, Trump's tweets and online Trends are correlated, and both time series contain information that can
predict the other (cf. Granger causality). A focus on the first tweet suggests that rather than the tweets causing public online interest
or vice versa, it is quite likely that external events were the real cause of interest. This closer analysis was only conducted on one
of his tweets and for one topic, however. The results should therefore be interpreted with caution, and a more systematic study should
be done to generalize our observations.

## Can we Predict Trump's Influence? Or his Tweeting Behaviour?

So far, we have demonstrated the difficulty of establishing a causal link between Trump's tweets and general online trends, or
vice versa. To shed more light on Trump's influence and on his tweeeting habits, we will conduct the following analyses.

First, we would like to investigate whether we can predict the number of retweets by Trump's followers using variables such as the tweet's sentiment
and its topic.

In a second step, we will try to wee whether we can predict the sentiment of Trump's tweets using external signals: the overall sentiment of
American tweets and the rise of Covid cases in the US.

### Sentiment Analysis of Trump's Tweets

<div class="internet">
    <img src="assets/img/sentiment_pie_chart.png" style="display: block; margin: 0 auto; width: 30%;"/>
</div>

To comprehend the general sentiment of Trump's tweets, we used VADER, a rule-based sentiment analyzer specific
for social media text. Each tweet is assigned a score calculated as the aggregate of individual word scores within the
text. Our analysis will focus on compound scores, which are a combination of positive, negative, and neutral scores.

Our findings indicate a predominately positive sentiment in Trump's tweets. This observation could have two
potential explanations:

- As a politician, Trump might be inclined to emphasize positive events over negative ones in his tweets. Highlighting
  favorable occurrences concerning himself or his voters could serve as a making a case for voting himself, such as :

<p>"The 75,000,000 great American Patriots who voted for me, AMERICA FIRST, and MAKE AMERICA GREAT AGAIN, will have a GIANT VOICE long into the future. They will not be disrespected or treated unfairly in any way, shape or form!!!"</p> 

- The VADER lexicon might be inaccurate for capturing the sentiment of sarcastic tweets. Despite VADER's focus on social
  media language, discerning sarcasm remains a challenging task, potentially introducing biases in the analysis. As an
  example, the following tweet is considered positive by VADER:

<p>"mike pence didn’t have the courage to do what should have been done to protect our country and our constitution  giving states a chance to certify a corrected set of facts  not the fraudulent or inaccurate ones which they were asked to previously certify  usa demands the truth" </p> 

Our strategy for assessing VADER's capability to interpret Trump's sentiment consists in focusing on tweets related to other
topics, for example Joe Biden and Democrats. We expect a negative sentiment given that they are the main target of
Trump's tweets. Yet,
when observing the plotted data, while a slight shift in sentiment distribution is evident, the dominant sentiment
remains neutral or positive. We should therefore be careful in our upcoming analyses, since sarcasm could alter our
results.
Interestingly, looking at the graph below, only tweets associated with fake news in relation to COVID-19 exhibit a
notably strong negative sentiment. This aligns with expectations, since Trump's tweets concerning fake news usually serve
as attacks directed at Democrats, the establishment, and the media.

<div class="internet">
    <img src="assets/img/stacked_plot_sentiment_categories.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

### What kind of Tweet gets Trump most Retweets?

We have seen that Donald Trump is usually not a trend maker, but rather a trend follower. Still, he does propagate trends
to some extent, at least among his followers.
Let's use the number of retweets of his declarations to spot which types of tweets are more influential and spread. We
already noticed that Trump's tweet are compound in sentiments. Let's see what sentiments spread the most (uncertainty bars
represent 95 % confidence intervals):

<div class="internet">
    <img src="assets/img/retweet_per_sentiment.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

According to this plot, tweets with negative sentiment tend to be significantly more retweeted. As shown in part 2, those tweets might
refer to Democrats or other of his opponents. Let's dive into the average number of retweets  for a few different topic categories:

<div class="internet">
    <img src="assets/img/barplot_per_categories.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

Surprisingly, talking about Covid makes fewer retweets than his usual subjects, such as the Democrats or Joe Biden. Interestingly though,
tweets related to topics commonly associated with fake news (e.g. hydroxychloroquine) get more retweets on average.
Nonetheless, note that since the distribution of sentiments is different across categories, visually assessing the impact
of each of them separately is delicate. We can check the significance of the difference of average retweets by looking at
retweets for each category separately :

<div class="internet">
    <img src="assets/img/retweets_per_categories.png" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

Looking at this, we wondered: can we predict the impact of Trump's tweet using factors such as being Covid-related,
fake news-related or the tweet's sentiment ? Moreover, can we disentangle the impact of topic and
sentiment on the number of retweets?
When regressing number retweets versus sentiment types, being fake news-related (talking about one the
fake news topics we studied) and being related to Covid, we obtain the following results:

<div style="text-align: center;">
  <img src="https://latex.codecogs.com/png.image?\dpi{160}y_i=\beta_0+\beta_1&space;x_{fake-news-related}+\beta_2&space;x_{covid-related}+\beta_3&space;x_{sentiment-type}" alt="equation">
</div>


Here, intercept corresponds to the zero class, being not fake news related, not covid-related and neutral.

<div style="margin: auto; width: 50%;">
  <table>
    <thead>
      <tr>
        <th></th>
        <th>Coef</th>
        <th>Std error</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Intercept</td>
        <td>2.098e+04 (***)</td>
        <td>295.588</td>
      </tr>
      <tr>
        <td>C(covid_related)</td>
        <td>-4894.4386 (***)</td>
        <td>736.312</td>
      </tr>
      <tr>
        <td>C(is_fake_news)</td>
        <td>7912.5949 (***)</td>
        <td>1933.190</td>
      </tr>
      <tr>
        <td>C(NEGATIVE)</td>
        <td>2782.3507 (***)</td>
        <td>417.806</td>
      </tr>
      <tr>
        <td>C(POSITIVE)</td>
        <td>109.9182</td>
        <td>376.424</td>
      </tr>
      <tr>
        <td>R^2</td>
        <td>0.009</td>
        <td></td>
      </tr>
    </tbody>
  </table>
    <br>
  *p-values* : ***p<0.001, **p<0.01 and  *p<0.05
</div>



From this analysis, we can conclude that :

- Talking about covid significantly reduces the number of potential retweets
- However, a tweet related to fake news will significantly increase the number of potentiel retweets, higher than the
  decrease when talking about covid
- Negative sentiment in tweets spread significantly more than neutral ones
- However, we can not say that positive ones spread faster or slower than neutral ones

While not allowing a complete conclusion, these results support two classic opinions about information spread on social
media:

- Tweets with identified negative sentiment spread more than those with positive/neutral ones, which seems opposite to
  the New York Times'
  conclusion : [Good News Beats Bad on Social Networks](https://www.nytimes.com/2013/03/19/science/good-news-spreads-faster-on-twitter-and-facebook.html)
- Talking about fake news tends to create more impact than truth, which is consistent with the results of the following
  study: [On Twitter, false news travels faster than true stories](https://news.mit.edu/2018/study-twitter-false-news-travels-faster-true-stories-0308)

### Predicting the Sentiment of Trump's Tweets using Exogenous Factors

Now that we identified that some characteristics of Trump's tweet have a direct impact on their spread, we would like to
see whether we can predict one of these characteristics: the tweet's sentiment. As predictors of the sentiment of Trump's tweet, we use the mean
of the compounded sentiment score of daily american tweets, and the rise in new COVID-19 cases in the US. 
We focused on the timeframe spanning from March 19, 2020 to April 18, 2020.

Initially, we conducted separate regressions, regressing Trump's sentiment on each predictor individually. Both
predictors exhibited significance at a 5% level. Subsequently, taking a step forward, we incorporated both predictors
into the regression model. Notably, we retained the expected sign of the coefficients, and the p-values reduced compared
to the single-predictor regressions.

Below, we present the regression results in the following table.

#### Logistic regression (Trump's sentiment ~ general sentiment + increment of new cases)

<div style="text-align: center;">
  <img src="https://latex.codecogs.com/png.image?\dpi{130}&space;y(Trump's-sentiment)=\beta_0&plus;\beta_1&space;x_{general-sentiment}&plus;\beta_2x_{increment-of-new-cases}" alt="equation">
</div>
<div style="margin: auto; width: 50%;">
<br>
<table>
  <thead>
    <tr>
      <th></th>
      <th>Coef</th>
      <th>Std error</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Intercept</td>
      <td>-1.2070</td>
      <td>0.679</td>
    </tr>
    <tr>
      <td>people_sent</td>
      <td>4.8260 (*)</td>
      <td>2.069</td>
    </tr>
    <tr>
      <td>increase_new_cases</td>
      <td>-1.9933 (*)</td>
      <td>0.875</td>
    </tr>
    <tr>
      <td>R^2</td>
      <td>?</td>
      <td></td>
    </tr>
  </tbody>
</table>
<br>
*p-values* : ***p<0.001, **p<0.01 and  *p<0.05
</div>

We now want to assess the robustness of our logistic regression. Let's compute the confusion Matrix, the ROC curve and the
AUC score:

<div class="results">
    <img src="assets/img/conf_e_auc.jpeg" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

The results obtained are promising, demonstrating both precision and recall values at 0.8. Our analysis was conducted
within a month-long window, aligning with the peak period of interest in Trump's tweets about Covid-19.
The regression analysis used aggregated daily data, providing a more stable viewpoint compared to the volatility
inherent in individual tweets. However, extending this analysis over a more extended period might not work. As time
progresses, Trump's interest in Covid-related topics declined, resulting in a scarcity of daily data.

Moreover, this logistic regression demonstrated that the sentiment of Trump's tweets, a key factor influencing their retweet,
can be predicted from exogenous factors. This support the conclusion that Trump is not making trends, but rather following
the crowd and its sentiment.

# Conclusion:
This project studied the impact of Donald Trump's tweets during the Covid epidemic. This was a time of intense internet
traffic in which Trump was a very special tweeting character. Our main research interest was the impact of his tweets on the spread
of fake news. Specifically, was Trump a trendmaker or was he only following some hot topics
already present on Twitter? Put differently, was Trump influential enough to start the spread of a fake news? 

With the Causal Impact tool, we were able to demonstrate no precursor effect of Trump on the online trends of some identified
fake news. Looking more closely, it would seem that exogenous causes were actually the reason for the rise of interest in
a topic, and for Trump to tweet on that same topic. 

Following on the interest in fake news, we looked at our research question the other way
around: what properties of Trump's tweet would make it influential (i.e. being retweeted) and can we predict the
presence of these properties in tweets based on exogenous factors? We assessed the impact of sentiment and some selected topics on the
number of retweets. A regression allowed us to disentangle the impact of each on the number of retweets.  We observed a net increase of retweets for negative
tweets compared to neutral and positive ones. We also showed that some topics spread more easily than others. Finally, we saw that the sentiment
of Trump's tweets can be fairly well predicted from exogenous data, adding weight to our previously anticipated conclusion:

**Donald Trump had some influence on Twitter, particularly among his followers, but no demonstration of genuine large-scale trend making could be made:
he is more likely to have surfed on the trends of the time**

Finally, recall that our study might be more related to current news than it looks at first sight. Since August 24, Donald Trump is back on X (new
Twitter), showing his [mugface](https://twitter.com/donaldtrump) again as a sign of his return. Since he is running for president
again we may wonder: is he using the same communication patterns as we found in our study? We leave the question open (for now). In the meantime, 
while [The Economist](https://www.economist.com/leaders/2023/11/16/donald-trump-poses-the-biggest-danger-to-the-world-in-2024) argues that 
Trump poses serious threats to world stability, we should probably not worry too much: Trump promises to only be a dictator [on day one](https://eu.usatoday.com/story/news/politics/elections/2023/12/11/donald-trump-dictator-one-day-reelected/71880010007/) !

Concluding on this wise advice, thank you for reading our data story! We hope you found it interesting!


