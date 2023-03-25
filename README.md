# Changes in Twitch Streaming due to Covid
### Author(s): Brennan Copp & Isabel Sy,  March 2023  

[Project Overview](#project-overview)

[Data Processing (ETL)](#etl-process-and-database-design)

[Cleaning and Visualizing Data with Python](#analyzing-the-data-in-Python)

[Analyzing Cleaned Data](#analyzing-cleaned-data)

[Summary and Conclusions](#summary)

## Background
Live streaming, as the name suggests, is content broadcasted in real time on the internet. Platforms such as YouTube, TikTok, and Instagram offer this feature, but this was not always the case. Before streaming became what we now know it to be, only a few websites allowed users to have a live platform. One such website is Twitch.tv (Twitch). 

Created in 2011 and mostly catered around the gaming community, Twitch quickly grew to become one of the biggest live streaming platforms on the internet. A rise in the popularity of social media as well as the COVID-19 lockdown gave way for Twitch to grow. Now, Twitch streamers broadcast not only gaming but also music, sports, podcasts, and even food oriented content.

## Project Overview
Using data collected from Twitch onto a 3rd party website, we investigated relationships between streaming languages, years before, during, and after Covid, and follower count, view count, and total watch time for a top streamer within each streaming language of interest.

We used Python for all data processing, cleaning, and visualization.


### Resources
Data: [Twitch Performance Data](https://sullygnome.com/)
Software/Languages: Python 3.8.16 (Pandas Library, Matplotlib Library, Statsmodels Library)

## ETL Process and Database Design
Our dataset contains 45 csv files, obtained from [SullyGnome](https://sullygnome.com/). The site creator of SullyGnome (David) states in the About page that all data aggregated and sythensized on the site is from the Twitch API. 

Due to the project's time constraint, the data has the following limitations:
- Only specific top performing categories were chosen for analysis
- One top ranking Twitch channel within each streaming language was chosen to represent the streaming language as well as smaller channel performances

### Data Cleaning

## Analyzing the Data in Python

## Summary
