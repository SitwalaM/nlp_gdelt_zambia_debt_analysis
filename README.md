# Analysis on Sentiment Towards Zambia's Economic Debt using [GDELT Global Knowledge Graph Data](https://blog.gdeltproject.org/introducing-gkg-2-0-the-next-generation-of-the-gdelt-global-knowledge-graph/)

The aim of the analysis is to answer the following questions by considering data from 1st January 2021 to 17th April 2022

1. Has the sentiment towards economic debt changed for the better considering a change of government in August 2021?
2. Is there a clear difference in the tone in the mentions for the two presidents?
3. Can we identify different topics within the “ECON_DEBT” Theme in GDELT data and what effect do they have on sentiment?



Please see Full Notebook for analysis: [Notebook](https://github.com/SitwalaM/nlp_gdelt_zambia_debt_analysis/blob/main/notebooks/main_gdelt_zambia.ipynb)

## Some Context on the Debt Situation

In 2020 Zambia's debt was estimated at 128.7% of GDP ([source](https://countryeconomy.com/national-debt/zambia)). The debt had increased from 25% of GDP in 2012 to 94% of GDP in 2019 ([IMF Global Debt Database](https://www.imf.org/external/datamapper/datasets/GDD)). This poses a huge risk to the country's growth potential, this analysis seeks to find out if the change in governance has an effect on the sentiment towards the country's debt.  

<div align="center">
  
<img src="https://github.com/SitwalaM/nlp_gdelt_zambia_debt_analysis/blob/main/images/bar_graph_debt.png" width="450">
  
</div>


# Global Knowledge Graph Dataset
 Global Database of Events, Language, and Tone (GDELT) aims to capture what's happening in the world and the data is available on [Google Cloud Platform](https://cloud.google.com/bigquery). In this analysis, the Global Knowledge Graph Data (GKG) was used, a full description of the dataset can be found [here.](http://data.gdeltproject.org/documentation/GDELT-Global_Knowledge_Graph_Codebook-V2.1.pdf). The following columns were used for the dataset,
 
 <div align="center">
 
 | Field | Description |
|---|---|
| GKGRECORDID | Unique Identifier for each record which contains a date and time-stamp |
| V2Locations | Locations mentioned in the text. This field is filtered for Zambia  |
| Quotations | All quoations in the text are given here |
| V2Tone | Provides, the average tone, positive tone, negative tone and polarity |
| Persons | Persons mentioned in the text. (Used to filter out the two presidents) |
| V2Themes | Different themes are available, list can be found [here](http://data.gdeltproject.org/api/v2/guides/LOOKUP-GKGTHEMES.TXT). "ECON_DEBT" was used for this analysis|
  
</div>
  
# Average Tone Time-Series 

![tone-box-plots](https://github.com/SitwalaM/nlp_gdelt_zambia_debt_analysis/blob/main/images/tone_boxplots.png)
![tone-time-series](https://github.com/SitwalaM/nlp_gdelt_zambia_debt_analysis/blob/main/images/tone_time_rolling.png)


# Average Tone President Comparison: Hakainde Hichilema Vs Edgar Lungu

<div align="center">
  
<img src="https://github.com/SitwalaM/nlp_gdelt_zambia_debt_analysis/blob/main/images/tone_dist_presidents.png" width="450">
  
</div>


# NLP Topic Modelling within the Economic Debt Theme Category

![topic words](https://github.com/SitwalaM/nlp_gdelt_zambia_debt_analysis/blob/main/images/topic_words.PNG)

<div align="center">
  
<img src="https://github.com/SitwalaM/nlp_gdelt_zambia_debt_analysis/blob/main/images/topics_dist.png" width="400">
  
</div>

# Conclusions

1. Has the sentiment towards economic debt changed for the better considering a change of government in August 2021?

No significant change has been noticed, in fact in April 2022 the sentiment was the lowest it has been for a while.

2. Is there a clear difference in the tone in the mentions for the two presidents?

No siginificant difference is observed between Edgar Lungu and Hakainde Hichilema in the data, however, Edgar Lungu does show more records with a very low sentiment.

3. Two topics identified within the "econ_debt" theme. Topic 1 tone has less variance than topic 0.

## Future Work

The next step will be to use the data as a signal for forecasting models in conjuction with an outlier detection algorithm which picks out extreme tones in the dataset.




