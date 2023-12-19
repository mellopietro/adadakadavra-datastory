---
layout: home
title: Trump and COVID19
subtitle: Adadakadavra Team
---

# Context

<div class="title-background">
    <img src="assets/img/title.jpg" style="display: block; margin: 0 auto; width: 100%;"/>
</div>


Remember the beginning of 2020, Covid spread like an unprecedent wildfire. The disease was not unkwnon, not understood
and scary. Most of the countries decided to lockdown to stop the spread and protect their populations. This resulted in
major and global changepoints in mobility :

ADD PLOTS ABOUT THE MOBILITY

This time at home was ideal for cooking, watching cat videos (or play with your cats) and spending time on the internet.
Interestingly, the global internet traffic followed the mobility evolutions:

ADD PLOT AND CORRELATION THERE

Main area of searched topics has been studied, you can have a look to : .. . But internet traffic during covid time was
not only made of cooking recipes and cats, it also was a proper time for fake news propagation, or as
the [WHO](https://www.who.int/health-topics/infodemic#tab=tab_1) calls it,
an infodemic. The ancestor of X, Twitter was one of the biggest place to propagate information, especially when
everything was changing as fast as the premise of the covid crisis. We all know that not all people have the same voice
on Twitter, few of them are considered to be the most influential individuals on the network. If you had to bet on of
person to be influential on Twitter, who would it be?

**Take a few seconds and answer to yourself, who would it be?**

I don't know who you got in mind, but for us, it has to be Donald Trump. Before he was evicted from the network, he was
one of the most followed account (source?). If you don't remind his tweet's style, here is a refresher :
<img src="images/trump_sample_tweet.png">
We all know Donald Trump has spread fake news, especially on Twitter, his favorite communication channel.

TO MERGE :
Donald Trump’s many tweets during the Covid pandemic spread like wildfire, probably making him one of the most
influential figures during the pandemic – but in the end, was he that influential? Will causal analyses of the effect of
Trump’s tweets on Wikipedia and Google Trends pageviews show that he was leading or following online trends? Our
goal is to study the impact an influential leader can have on information spread in a
crisis with a focus on fake news, as an overload of misleading or contradictory
statements (an infodemic, as [WHO](https://www.who.int/health-topics/infodemic#tab=tab_1) calls it) are known to have a
detrimental impact on crisis
management. 
To provide a more comprehensive insight into Trump’s actual influence
on online information spread, we would then like to compare it with that of other
factors such as mobility restrictions or key milestones (e.g. first Covid death). 

### Trump the Trend Maker or Trump the Follower, that is the question!


## Donald Trump's tweets

## Who is causing whom? Let's study Donald Trump's favorite fake news

## What's the impact of topics and sentiment in the spread

# Introduction

The COVID-19 pandemic has been a global crisis of unprecedented scale and impact, disrupting lives, economies, and
societies around the world. It has been characterized by rapid spread, high case numbers, and significant mortality. The
pandemic has had a profound impact on healthcare systems, economies, education, and social and mental well-being.

### Impact on Healthcare Systems

The COVID-19 pandemic has placed a severe strain on healthcare systems worldwide. Hospitals have been overwhelmed with
patients, leading to shortages of beds, ventilators, and personal protective equipment (PPE). Healthcare workers have
been under immense pressure, working long hours and facing the risk of infection. The pandemic has also led to delays in
non-COVID-19 care, as hospitals have prioritized COVID-19 patients.

### Impact on Economies

The COVID-19 pandemic has caused a global economic recession, with GDPs shrinking in most countries. Businesses have
been forced to close or reduce their operations, leading to job losses and increased unemployment. The pandemic has also
disrupted supply chains and trade, further exacerbating the economic crisis.

### Impact on Education

Schools and universities have been closed for extended periods during the pandemic, disrupting education for students of
all ages. This has had a significant impact on learning outcomes, particularly for disadvantaged students. Online
learning has been offered as an alternative, but it has not been a perfect solution, as many students do not have access
to reliable internet or the necessary technology.

### Impact on Social and Mental Well-being

The COVID-19 pandemic has had a profound impact on social and mental well-being. The isolation and social distancing
measures required to control the spread of the virus have led to increased loneliness, anxiety, and depression. The
pandemic has also exacerbated existing social inequalities, as people from lower-income households and minority groups
have been more likely to experience job losses, food insecurity, and housing instability.

### Response to the Pandemic

In response to the pandemic, governments around the world have implemented a range of measures, including lockdowns,
travel restrictions, mask mandates, and social distancing guidelines. These measures have had varying degrees of success
in controlling the spread of the virus. Governments have also invested in vaccine development and distribution, with
over 69% of the world's population now fully vaccinated.

The COVID-19 pandemic has been a harrowing experience for humanity, but it has also brought about a renewed sense of
global cooperation and solidarity. The pandemic has shown the importance of strong public health systems, robust
economic policies, and social cohesion in responding to global crises.

### Mobility

During state quarantines and lockdowns, people were forced to stay at home, leading to a sharp decline in mobility. This
was reflected in a drop in traffic congestion, public transportation usage, and retail foot traffic. For example, data
from Apple Mobility Trends showed a 95% decrease in visits to retail and recreation categories in New York City during
the peak of the pandemic.

<div class="mobility">
    <img src="assets/img/preview_mobility.png" style="display: block; margin: 0 auto; width: 60%;"/>
</div>

### Internet Consumption

In contrast, internet consumption skyrocketed during state quarantines. As people were spending more time at home, they
turned to the internet for work, education, entertainment, and communication. This led to increased traffic on websites,
social media platforms, and video streaming services. For instance, Zoom's daily user meetings increased from 10 million
in December 2019 to 300 million in April 2020, demonstrating the surge in remote work and online communication during
the pandemic.

<div class="internet">
    <img src="assets/img/preview_internet.png" style="display: block; margin: 0 auto; width: 60%;"/>
</div>

The increase in internet usage also highlighted the importance of reliable internet connectivity. Many people found
themselves struggling to access high-speed internet, which hindered their ability to work, learn, and stay connected
with loved ones. This underscored the need for improved internet infrastructure and equitable access to broadband
services.

The changes in mobility and internet consumption during the pandemic have had far-reaching consequences. They have
reshaped how people work, learn, socialize, and engage with the world around them. As we continue to navigate the
pandemic and its aftermath, understanding these changes will be crucial for designing future strategies for urban
planning, digital infrastructure, and social support systems.


# Does Trump cause Online Trends?
One of our research questions is to find whether there is a causal relationship between Trump's tweets and the number
 of visits on some Covid-related topics, for example hydroxychloroquine on Wikipedia. During COVID-19 period Trump 
 claimed that Hydroxychloroquine was a cure for COVID-19. This claim was not supported by scientific evidence, 
 making it more of a fake news. This was further motivation to investigate this topic in particular.

### Step 1: A first graphical inspection of the evolution of online trends and Trump's tweeting
We want to get the global number of pageviews for the article related to hydroxychloroquine from Wikipedia. 
We will start by graphically studying the evolution of the number of queries/visits to assess whether 
Trump's tweets had an impact on them.

<div class="internet">
    <img src="assets/img/hydro_wiki_timeseries_daily.png" style="display: block; margin: 0 auto; width: 60%;"/>
</div>

As we can see from the graph above, Trump's tweets on hydroxychloroquine seem to precede certain attention 
peaks (e.g. the second big peak at the start of April), but come after others (e.g. the first big peak, around mid-March). 
A possibile explanation is simply that the tweets sometimes cause attention, whereas other times public interests makes Trump's
 tweet about the topic. Another one is that both are caused by external factors, and that Trump's and the public's reaction 
 times vary: sometimes Trump reacts the fastest, and other times the public does.

### Step 2: Granger causality - Do Trump's tweets give useful information to predict online interest?
To better understand Trump's potential causal impact on online trends, we will focus on the topic of hydroxychloroquine. 
The plot of daily Wikipedia views made it difficult to assess whether Trump causes tweets or the other way around. 
To investigate this, we therefore chose to conduct a [Granger causality](https://en.wikipedia.org/wiki/Granger_causality) test. 

"The Granger causality test is a statistical hypothesis test for determining whether one time series is useful in forecasting 
another". The [null hypothesis](https://www.statsmodels.org/dev/generated/statsmodels.tsa.stattools.grangercausalitytests.html) 
is that "the the time series the first column is NOT Granger caused by the time series in the other columns".

We conducted two Granger causality tests: "Trump's Granger causes views on Wikipedia" and "Views on Wikipedia Granger cause
 Trump's tweets". The p-values of the test for one and two lags are given in Table TODO. According to [Wikipedia](https://en.wikipedia.org/wiki/Granger_causality),
  however, "the null hypothesis of no Granger causality is not rejected if and only if no lagged values of an explanatory 
  variable have been retained in the regression". In other words, having signifance for one lagged value is enough. 

Both Granger causality tests have at least one lagged value for which the p-value is below the threshold of 0.05. 
Both tests are therefore statistically signifcant: Trump's tweets Granger cause Wikipedia views and vice versa.

How to interpret the fact that the two time series Granger cause each other? As mentioned earlier, Granger causality just
 means that one time series is useful at predicting the other. There can therefore be two explanations to our results:
- sometimes Trump causes tweets, other times public interest causes Trump to tweet;
- or both time series are actually caused by external factors. Sometimes Trump's reacts faster, and sometimes the public 
get interested first. The varying reaction times could explain the Granger causality results.

### Step 3: Causal Impact - A tool to assess the impact of one of Trump's tweets on online trends
To further investigate whether Trump's tweet cause views, we will focus on his first tweet, which coincides with a big peak
in interest (both on Wikipedia and Google).
The [Causal Impact](https://google.github.io/CausalImpact/CausalImpact.html) library in Python allows us perform a test which
 can tell us if there is a causal relation between Trump's first tweet and the number of Google queries on Hydroxychloroquine. 
 We are focusing on Google Trends, as they allows us to study time series at hourly granularity. 
To run this analysis we need to build a dataframe with the following columns:
- data index: the date of the observation of our time series.
- y: the number of visits to the the page of Hydroxychloroquine (test variable).
- x: the number of visits to a set of pages (the control variables), which were not affected by the intervention (Trump's first tweet).

The following [assumptions](https://pypi.org/project/pycausalimpact/) need to be verified to conduct this test : "the response 
variable can be precisely modeled by a linear regression with what is known as "covariates" (or X) that must not be affected by 
the intervention that took place".

We decided to take the time series of the following five topics, which for obvious reasons should not have been affected by 
Trump's tweet, as control variables: climate, coffee, news, shop and time.

We focused on the first of Trump's tweets mentioning hydroxychloroquine, as it happens to coincide with a pig beak in online 
interest for the topic. 
The causal impact analysis for this first tweet corroborated the visual inspection of the Wikipedia time series: the peak in
interest on hydroxychloroquine preceded Trump's first tweet. His tweet therefore didn't seem to have had a strong impact on interest. 
Note, however, that we used global trends time series. It might be that Trump had a local impact (though probably not strong) on 
Google searches, e.g. in the United States.

As explained earlier, an alternative possibility to explain why online trends time series and Trump's tweets Granger cause each 
other is that an external factor is the "real" cause of the surge of interest.

Some online research revealed that the big peak in interest mid-March might have caused by the two following major events, 
which both took place on March 16, 2020:
- a mobility changepoint in the United States following restrictions, according to [Manoel et al.](https://arxiv.org/abs/2005.08505),
- "A study on the use of hydroxychloroquine in patients with SARS-CoV-2 was published (online via Youtube) - The preliminary data from 
this small study was heard round the world", as quoted from [Saag et al.](https://jamanetwork.com/journals/jama/fullarticle/2772921).

We therefore tried to reconduct a causal impact analysis, considering March 16, 5 P.M. (GMT, so between 9 A.M and 12 A.M. in the USA)
 as our intervention time. The resulting plot can be seen in Figure TODO.

<div class="internet">
    <img src="assets/img/causal_plot.png" style="display: block; margin: 0 auto; width: 60%;"/>
</div>

The causal impact analysis shows that the intervention on March 16 (the mobility restrictions, the publication or both - perhaps even
 other events, this period was quite hectic) has a strong impact on Google Trends searches on Wikipedia. 

In conclusion, Trump's tweets and online Trends are correlated, and both time series contain information that can predict the other
 (cf. Granger causality). A focus on the first tweet suggests that rather than the tweets causing public online interest or vice versa,
 it is quite likely that external events were the real cause of interest. This closer analysis was only conducted on one of his tweets
  and for one topic, however. The results should therefore be interpreted with caution, and a more systematic study should be done to 
  generalize our observations.


