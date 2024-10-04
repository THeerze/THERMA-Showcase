# How can biking routes be optimized to keep Amsterdam residents in the shade during heat events? 
## THERMA - team for heat exposure reduction and mitigation in amsterdam
*Ameer, Gonzalo, Kian, Sahir, Teun, Tom*

## Project overivew

This repository contains the code developed for our research project on heat stress that we conducted in collaboration with the GGD Amsterdam (Public Health Service Amsterdam). It includes a scraper for acquiring NOS news articles and comments from NU.nl (both Dutch sources) as well as the processing of geospatial data related to shade and perceived temperature. This data was mapped onto the Amsterdam street network of OpenStreetMap. Additionally, the repository includes code for topic modeling NOS narratives around heat stress, sentiment analysis of NU.nl comments, and geospatial analysis of Amsterdam’s bike network. Our findings are presented in a report where we propose an intervention plan aimed at optimizing biking routes for shade during heat events. Feel free to reach out if you’re interested in the project or would like to discuss the code and analyses!

## Executive Summary

This study presents a data-driven approach to mitigating the risks of heat stress for cyclists in Amsterdam.
Through a literature review, the study identifies shade cover as a critical tool towards climate adaptation.
By combining ethnographic observations, natural language processing, and geospatial analysis, we
develop a methodology to assess the state of heat stress in Amsterdam. By performing topic modelling on
news articles, sentiment analysis on comments, and geospatial analysis on heat and shadow, we identify
leverage points for change.
The paper leverages systems thinking and social practice theory to develop a three-faceted intervention
experiment. The intervention experiment involves an awareness campaign, a real-time heat-aware route
planner, and the redirection of cyclists to heat-safe streets. It offers practical recommendations and future
steps for organisations like the GGD Amsterdam, Climate Adaptation Services, and urban planners to
prepare the city for rising temperatures and recraft the social practices of cycling in Amsterdam.

## important notes/files:

Heat_metric:
- for the heat metric analysis, two raster images are loaded from the Klimaateffectatlas folder. Due to large file size these couldn't be hosted on Github
- featureCalc.ipynb is used to create the bike_network.csv
- analysis.ipynb contains the regression model

nos_topic modelling:
- articles.df.csv contains all scraper articles from the keyword search (nos_keyword_scraper)
- in the analysis folder, LDA_model_analysis includes our test of an LDA model, and analysis_BERTopic contains the final model

nunl_scraper:
- all_comments.csv is the main used data file
- analysis of the comments is done in the sentiment_analysis folder

sentiment_analysis:
- analysis conducted in order topic_modelling -> translate -> sentiment_analysis
- final data visualisations are contained in the sentiment_analysis notebook

## Project Preview

### Geospatial analysis

<img src="heat_metric/graphs/after%20removing%20small%20streets.png" width="500"/>

*Fig 1: Extract of the Amsterdam bike network used in the analysis*

<img src="heat_metric/graphs/raster%20cropping%20shade.png" width="500"/>

*Fig 2: Raster cropping of shade*

<img src="heat_metric/graphs/bike%20network%20shade%20proportions.png" width="500"/>

*Fig 3: Shadow proportion mapped onto the bike network*

### NOS topic modelling

<img src="nos_topic_modelling/graphs/8%20most%20frequent%20topics.png" width="500"/>

*Fig 4: 8 most frequent topics*

<img src="nos_topic_modelling/graphs/topics%20over%20time.png" width="500"/>

*Fig 5: Topics over time*

<img src="nos_topic_modelling/graphs/example%20image%20topic%20modelling.png" width="500"/>

*Fig 6: Example topics of multimodal analysis*

### Sentiment analysis

<img src="sentiment_analysis/graphs/boxplot%20by%20topic.png" width="500"/>

*Fig 7: Boxplot of sentiment scores by topic*

<img src="sentiment_analysis/graphs/sentiment%20scores%20over%20time.png" width="500"/>

*Fig 8: Sentiment scores by topic over time*