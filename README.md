# Changes In TWITCH Streaming Due To COVID-19
### Author(s): Brennan Copp & Isabel Sy,  March 2023  

[Project Overview](#project-overview)

[Data Processing (ETL)](#etl-process-and-database-design)

[Cleaning and Visualizing Data with Python](#analyzing-the-data-in-Python)

[Analyzing Cleaned Data](#analyzing-cleaned-data)

[Summary and Conclusions](#summary)

![logo](https://1000logos.net/wp-content/uploads/2018/10/Twitch-logo.png)

## Background
Live streaming, as the name suggests, is content broadcasted in real time on the internet. Platforms such as YouTube, TikTok, and Instagram offer this feature, but this was not always the case. Before streaming became what we now know it to be, only a few websites allowed users to have a live platform. One such website is Twitch.tv (Twitch). 

Created in 2011 and mostly catered around the gaming community, Twitch quickly grew to become one of the biggest live streaming platforms on the internet. A rise in the popularity of social media as well as the COVID-19 lockdown gave way for Twitch to grow. Now, Twitch streamers broadcast not only gaming but also music, sports, podcasts, and even food oriented content.

## Project Overview
Using data collected from Twitch onto a 3rd party website, we investigated relationships between streaming languages, years before, during, and after COVID, and follower count, view count, and total watch time for a top streamer within each streaming language of interest.

We used Python for all data processing, cleaning, and visualization.


### Resources
Data: [Twitch Performance Data](https://sullygnome.com/)

Software/Languages: Jupyter Notebook - Python 3.8.16 (Pandas Library, Matplotlib Library, Statsmodels Library)

## ETL Process and Database Design
Our dataset contains 45 csv files, obtained from [SullyGnome](https://sullygnome.com/). The site creator of SullyGnome (David) states in the About page that all data aggregated and sythensized on the site is from the Twitch API. 

Due to the project's time constraint, the data has the following limitations:
- Only specific top performing categories were chosen for analysis
- One top ranking Twitch channel within each streaming language was chosen to represent the streaming language as well as smaller channel performances

### Data Cleaning
Data cleaning was fairly simple. 
A jupyter notebook with pandas imported was utilized to import the CSVs into a two dataframes, one for Twitch categories and the other for streamers.

Data for categories includes the top 100 games watched from 2018-2019 in English, Chinese, Korean, and Portuguese. From there, we narrowed it down to 4 categories: 2 online games(Fortnite & League of Legends), Just Chatting, and Music. 

![snip1](https://github.com/itsy24/Twitch_Success/blob/isy/images/snippet1%20.png)

From there, watch time per language were isolated and sorted by year.

![snip1](https://github.com/itsy24/Twitch_Success/blob/isy/images/snippet2.png)

## Analyzing the Data in Python

The graphs below show watch time(min) trends over the course of the 5 years and the total watch time for each langauge. 
As time passes, the viewership of Twitch for all 4 langauges rose, with English being streamed the most. 

![graph0](https://github.com/itsy24/Twitch_Success/blob/main/Graphs/watch_time_trends.png)
![graph00](https://github.com/itsy24/Twitch_Success/blob/main/Graphs/total_watch_time.png)

These graphs compare the 4 streamed languages and categories. 
As COVID began, the category 'Just Chatting' rose compared to the other categories who either decreased in streams or plateaued. 

![graph1](https://github.com/itsy24/Twitch_Success/blob/main/Graphs/popular_cat_eng.png)
![graph2](https://github.com/itsy24/Twitch_Success/blob/main/Graphs/popular_cat_pr.png)
![graph3](https://github.com/itsy24/Twitch_Success/blob/main/Graphs/popular_cat_cn.png)
![graph4](https://github.com/itsy24/Twitch_Success/blob/main/Graphs/popular_cat_kr.png)

Finally, statistcal analysis was done with a two-way ANOVA.

The test below demonstrates that language (p-value = 1.080788e-11) statistcally affects watch times more than what game/category is being streamed.

![ANOVA2](https://github.com/itsy24/Twitch_Success/blob/isy/images/anova2.png)

## Summary

### Conclusions based on our analysis

- Watch time increased for all streaming languages during 2020, indicating that COVID had an impact on Twitch's online traffic. 
- In 2021 English streaming for' Just Chatting' plateaued; most likely due to COVID restrictions being lessened in countires where English is the primary language spoken.  


