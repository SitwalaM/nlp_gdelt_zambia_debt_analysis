# Analysis on Sentiment Towards Zambia's Economic Debt using [GDELT Global Knowledge Graph Data](https://blog.gdeltproject.org/introducing-gkg-2-0-the-next-generation-of-the-gdelt-global-knowledge-graph/)

The aim of the analysis is to answer the following questions by considering data from 1st January 2021 to 17th April 2022

1. Has the sentiment towards economic debt changed for the better considering a change of government in August 2021?
2. Is there a clear difference in the tone in the mentions for the two presidents ?

## Some Context on the Debt Situations

In 2020 Zambia's debt was estimated at 128.7% of GDP ([source](https://countryeconomy.com/national-debt/zambia)). The debt had increased from 25% of GDP in 2012 to 94% of GDP in 2019 ([IMF Global Debt Database](https://www.imf.org/external/datamapper/datasets/GDD)). This poses a huge risk to the country's growth potential, this analysis seeks to find out if the change in governance has an effect on the sentiment towards the country's debt.  

[Insert the Graphs on the debt situation here]


# Global Knowledge Graph Dataset
 Global Database of Events, Language, and Tone (GDELT) aims to capture what's happening in the world and the data is available on [Google Cloud Platform](https://cloud.google.com/bigquery). In this analysis, the Global Knowledge Graph Data (GKG) was used, a full description of the dataset can be found [here.](http://data.gdeltproject.org/documentation/GDELT-Global_Knowledge_Graph_Codebook-V2.1.pdf). The following columns were used for the dataset,
 
 | Field | Description |
|---|---|
| GKGRECORDID | Unique Identifier for each record which contains a date and time-stamp |
| V2Locations | Locations mentioned in the text. This field is filtered for Zambia  |
| Quotations | All quoations in the text are given here |
| V2Tone | Provides, the average tone, positive tone, negative tone and polarity |
| Persons | Persons mentioned in the text. (Used to filter out the two presidents) |
| V2Themes | Different themes are available, list can be found [here](http://data.gdeltproject.org/api/v2/guides/LOOKUP-GKGTHEMES.TXT). "ECON_DEBT" was used for this analysis|

# Average Tone Time-Series 


# Average Tone President Comparison: Hakainde Hichilema Vs Edgar Lungu


# NLP Topic Modelling within the Economic Debt GDELT Category


# Conclusions

# Credits


