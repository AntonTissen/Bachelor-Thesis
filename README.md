# Bachelor-Thesis

Abstract:This bachelor's thesis explores how political actors and the sentiment they disseminate on Twitter shape the public's perception of the Ukraine war. By employing sentiment analysis using the VADER tool, network analysis, and statistical tests, the study examined the influence of key actors such as official political channels, news agencies, and prominent figures like Volodymyr Zelensky and Vladimir Putin. The majority of the analyzed corpus exhibited a predominantly negative sentiment (-80.145%). A detailed examination of the mentions in tweets about Zelensky and the official Kremlin account revealed significant disparities in the sentiment of the published content. The calculation of the Pearson correlation coefficient of -0.00376 and the p-value of 0.45188 indicate that there is no statistically significant linear relationship between the sentiment of the tweets and user interaction. This suggests that other factors, such as the specific content of the tweets or external events, may have a more profound impact on user reactions. Overall, this study provides an initial insight into the discourse structure during the first week of the war, although the dataset is limited and thus only captures a fragment of the broader discussion.
This repository contains the Python code used to analyze Twitter data for my Bachelor's thesis. The code performs the following key tasks:

1.  **Data Loading and Preprocessing:** Loads the Twitter data and cleans the text by removing URLs, mentions, hashtags, and non-alphanumeric characters.  It also filters tweets to include only those written in English.
    * `code/analysis.py` (or `main_analysis.ipynb`) contains the main analysis code.
    * Data is assumed to be in `data/sample_data.csv` (a small sample is provided).
    * **Data Source:** Dataset found on Kaggle.com via https://www.kaggle.com/datasets/foklacu/ukraine-war-tweets-dataset-65-days?select=Ukraine_war.csv
    * In my Thesis 40.000 tweets were analyzied. 

2.  **Sentiment Analysis:** Calculates the sentiment of the tweets using the VADER sentiment analysis tool.
    * VADER is used because it has a spezialization on short text, common in social media posts, primary on X/Twitter.
    * The sentiment is scored into negative, neutral, positive, and compound scores.

3.  **Network Analysis:** Constructs a network of Twitter users based on mentions and calculates network metrics such as degree centrality, betweenness centrality, and closeness centrality.
    *Network analysis helps to uncover patterns and relationships within a network.
    *Degree centrality indicates how many direct connections a node has.
    *Betweenness centrality indicates how often a node lies on the shortest path between other nodes.
    *Closeness centrality indicates how quickly a node can reach all other nodes in the network.

4.  **Statistical Analysis:** Performs a Pearson correlation analysis to examine the relationship between sentiment and user engagement (e.g., likes).
    * The Pearson correlation coefficient measures the strength and direction of a linear relationship between two variables.
    * The p-value indicates the probability that the observed results occurred by chance under the null hypothesis.

5.  **Analysis of Specific Actors:** Analyzes the sentiment of tweets mentioning key political actors (e.g., Volodymyr Zelenskyy and the Putin).
    * This analysis focuses on also on the Presidents of both countries. It is important how the people on social media react towards to the Presidents during wartime. 
