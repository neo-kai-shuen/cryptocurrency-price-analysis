# Cryptocurrency Price Analysis

## Nanyang Technological University - CZ4079 Final Year Project

## Official publication
[Cryptocurrency Price Analysis](https://dr.ntu.edu.sg/entities/publication/0b9fb091-8177-482c-90d0-a4794fbc36e8) 

#### Problem
Bitcoin, the world’s first and largest decentralized cryptocurrency, experiences extreme price volatility influenced by a range of factors. Among these, news events have been observed to significantly impact its price, as public sentiment shaped by news can drive market behavior. Despite its growing adoption as a payment method and investment tool, there is limited understanding of which specific types of news events most strongly affect bitcoin prices. This project aims to investigate the correlation between news sentiment and bitcoin price, identifying the news categories that exert the greatest influence.


#### Data source
The project uses two primary data sources:

CoinMarketCap – Provides historical bitcoin prices (12 April 2019 to 13 March 2020), including Date, Open, High, Low, Close, Volume, and Market Cap in USD. Data quality was verified and formatted appropriately for analysis.

Reuters – Supplies news headlines related to “Bitcoin” and “Cryptocurrency” across Business and Market topics for the same period. Extracted data includes Date and Title, with duplicate titles preserved due to differences in content.


#### Approach
The project workflow involves:
1. Collecting bitcoin price data from CoinMarketCap.
2. Web scraping news titles from Reuters covering Business, Market, and Bitcoin-related news.
3. Performing sentiment analysis on news titles to assign positive, neutral, or negative scores.
4. Conducting correlation analysis between bitcoin prices and news sentiment scores.
5. Performing time series analysis to visualize bitcoin price trends against news sentiment.
6. Drawing inferences to identify which types of news events most strongly influence bitcoin price.


#### Analysis
The project employs three main analytical methods:
1. **Sentiment Analysis** – Using Python’s NLTK library and VADER (Valence Aware Dictionary and sEntiment Reasoner), news titles are evaluated for sentiment polarity. Each title receives a compound sentiment score based on intensity and tone, accounting for factors such as punctuation, capitalization, degree modifiers, conjunctions, and preceding tri-grams. This quantifies the positive, neutral, or negative sentiment of news events.
2. **Correlation Analysis** – Conducted in R, correlation analysis measures the strength of the relationship between bitcoin prices and news sentiment scores. Correlation coefficients are calculated for bitcoin price vs Business News sentiment, Market News sentiment, and Bitcoin News sentiment to identify which types of news most strongly influence bitcoin price.
3. **Time Series Analysis** – Bitcoin price data and sentiment scores are plotted over time to visualize trends, fluctuations, and the interrelationship between news sentiment and price movements. Candlestick charts and time series plots help illustrate general pricing trends and potential predictive patterns.


#### Key results
1. **Sentiment Scores** – News titles were classified as Positive (≥0.5), Neutral (≥0 and <0.5), or Negative (<0). Daily sentiment scores were calculated by summing individual news scores, providing an overall sense of market sentiment. Different news categories (Business, Market, Bitcoin-related) yielded varying daily sentiment scores, indicating that no single category alone fully explains bitcoin price movements.

2. **Correlation Analysis** – Correlation coefficients between bitcoin prices and sentiment scores were generally weak across all news categories. While overall sentiment appeared not to significantly affect bitcoin prices, specific high-impact news events (e.g., market turmoil during the COVID-19 outbreak on 12–13 March 2020) caused sharp price fluctuations, suggesting that bitcoin responds more to targeted significant events than to aggregated sentiment.

3. **Time Series Analysis** – Bitcoin price trends showed periods of rise and fall over the study period. Time series plots of sentiment scores did not show clear trends, and plotting bitcoin prices alongside sentiment scores revealed no distinct correlation. Observations suggest that bitcoin price changes are influenced by specific contextual news events rather than general sentiment patterns.


#### Conclusion
This project investigated the correlation between news events and bitcoin prices. Sentiment analysis of news provides a sense of overall market optimism or pessimism, but no single news category consistently drives bitcoin price changes. The analysis indicates that news creating market uncertainty—particularly regulatory announcements or major financial events—has the strongest impact on bitcoin prices. Challenges included extensive news scraping and data cleaning, which were time-intensive. Future improvements could focus on isolating clusters of high-impact news events for clearer correlation analysis and applying ARIMA or SARIMA models for time series forecasting of bitcoin prices.


#### Technical stack
The project was implemented primarily using Python, leveraging its extensive ecosystem for data analysis, web scraping, and natural language processing. The key components of the technical stack include:

Python Libraries:
- pandas and NumPy for data manipulation and numerical operations.
- Matplotlib and Seaborn for data visualization and plotting time series.
- NLTK and VADER for Natural Language Processing and sentiment analysis.
- Requests and BeautifulSoup for web scraping news headlines.
- SciPy and statsmodels for statistical and correlation analysis.

Development Environment:
- PyCharm for Python coding, debugging, and project management.
- RStudio for additional correlation analysis and statistical operations.
- Microsoft Excel for preliminary data inspection, cleaning, and formatting.

This stack enabled the collection, processing, and analysis of bitcoin prices and news sentiment efficiently, while supporting visualization and statistical evaluation of relationships between variables.


#### Data visualisations


