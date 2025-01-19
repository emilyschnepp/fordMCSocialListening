#Social Listening with Reddit API and Ford Motor Company
<h1>Ford Social Listening w/ Competitor Analysis and Sentiment Forecasting<h1>

<h6>Note: This project is not affiliated with or endorsed by Reddit or Ford Motor Company</h6>

<h2>Key Highlights</h2>
• Queried over 5,000 Reddit posts across 6 subreddits and 13 car brands, spanning 2015–2024, to better understand Ford’s perception. <br>
• Used Prophet for time series forecasting to predict positive sentiment trends for Ford, achieving an MAE of 4.329. <br>
• Found that trust was the most dominant positive emotion, while fear was the most dominant negative emotion in Reddit conversations. <br>
• Ford’s post volume on Reddit grew sharply in 2024, surpassing GM and Stellantis for the first time. <br>
• Created detailed visualizations to showcase sentiment trends, competitor analysis, and subreddit-specific insights to guide marketing strategies. <br>
• Recommended leveraging trust-driven campaigns during positive sentiment peaks (Q3 2025) and preparing messaging to address fear narratives during neutral or negative periods (Q4 2025). <br>

<h2>Business Use Case:</h2> 
The prediction of positive sentiment with Prophet allows Ford Motor Company to anticipate changes in online perception and strategically schedule marketing campaigns and product announcements.
<br>
<br>
While the focus of this project is Reddit data, it can be expanded to include other platforms like Facebook, Instagram, Twitter, or even TikTok, each of which would provide more insight into how Ford is perceived digitally. For the purpose of this project, Reddit is decidedly sufficient as there was no cost associated with gathering Reddit data using the API. 

<h2>Project Goal</h2>
The purpose of this project is to explore Reddit posts to better understand Ford Motor Company’s reputation on the platform, and to compare its reputation to that of its competitors (GM and Stellantis). Also looked at leading models compared to competitors and predicted positive sentiment analysis. 

<h2>Prerequisites</h2>
• Reddit API credentials <br>
• Python <br>
• Pandas <br>
• NLTK: corpus – stopwords, tokenize – word_tokenize, stem – WordNetLemmatizer. <br>
• Sklearn: TFidfVectorizer, CountVectorizer, LatentDirichletAllocation, KMeans, TSNE, mean_absolute_error, mean_squared_error, silhouette_score. <br>
• Textblob, NRCLex, prophet, matplotlib, wordcloud, numpy, re, logging. Nltk punkt, stopwords, wordnet. <br>

<h2>Data Sources</h2> 
The following subreddits and car brands were combined for queries. <br> 
• cars (subreddit) <br> 
• trucks (subreddit) <br> 
• whatcarshouldIbuy (subreddit) <br> 
• askcarguys (subreddit) <br> 
• electricvehicles (subreddit) <br> 
• AskMechanics (subreddit) <br> 
• Ford, Lincoln (car brands) <br> 
• Chrysler, Dodge, Jeep, Ram, Fiat (car brands) <br> 
• General Motors, GM, Chevy, Chevrolet, Cadillac (car brands) <br> 
Methodology: Queried 500 posts per subreddit/brand and concatenated them into a master dataset.<br> 

![Percent Yearly Sentiment with Total Post Count](https://github.com/emilyschnepp/fordMCSocialListening/blob/14892cb1a2ee51ce835c1f05bda30386fd02fabe/visualizations/FMCPercYearlySent.png)
<br>
The visualization above highlights the growth in Reddit discussions over time, including trends in sentiment and total post volume.

<h2>Time Frame</h2>
The posts were dated between January 12, 2015 and December 7, 2024.
<h2>Models and Methods:</h2> 
<h4>Key Methods:</h4> 
• Customering with KMeans (e.g., identifying patterns in F-150 posts). <br>
• Time series forecasting with Prophet to predict positive sentiment trends. <br>
• Sentiment analysis using TextBlob. <br>
• Emotion analysis using NRCLex for fear and trust. <br>

![Positive Sentiment Forecast with Prophet](https://github.com/emilyschnepp/fordMCSocialListening/blob/14892cb1a2ee51ce835c1f05bda30386fd02fabe/visualizations/FMCProphetPredict.png)
<br>
The visualization above shows the sentiment forecast made with Prophet.
<br>
<h2>Data Preprocessing</h2> 
• Text Cleaning and Tokenization – removing stopwords, converting all text to lowercase, removing punctuation, lemmatization (reducing words to their root), and rebuilding strings post-tokenization. <br>
• Lemmatization was chosen for normalization as it retains the meaning of the words, even after reducing them to their root word. <br>
• Used NRCLex to identify the emotions present in each post, like trust or fear. <br>
• Determined sentiment analysis using TextBlob. <br>

<h2>Metrics</h2>
Mean Absolute Error (MAE) of 4.329. 

<h2>Visualizations</h2> 
• Sentiment Over Time: Dual axis line chart showing percentage of sentiment and total posts. Intended to highlight changes in sentiment over time. <br>
• Sentiment by Subreddit: Bar chart gauging posts per sentiment across subreddits. Intended to show variations in sentiment across subreddits. <br>
• Side-by-Side Word Cloud: Identifies emotionally charged words related to trust and fear. <br>
• Trust and Fear by Subreddit: Bar chart comparing trust and fear across subreddits. <br>
• Sentiment Forecasting: Forecasted sentiment using Prophet and highlighted peaks and valleys. Intended to guide decisions. <br>

Detailed visualizations and their interpretations can be found in the project PowerPoint presentation: <br>

[PowerPoint Presentation](https://github.com/emilyschnepp/fordMCSocialListening/tree/14892cb1a2ee51ce835c1f05bda30386fd02fabe/presentation)

<h2>Findings</h2> 
<h4>Sentiment Trends:</h4>
• Neutral sentiment dominates (~70-80%), followed by positive (~20%), and negative (<20%). <br>
• Positive sentiment has grown steadily, while post volume spiked in 2024. <br>
<h4>Subreddit Sentiment:</h4>
• r/Ford has higher positive and neutral sentiment than others. <br>
• r/electricvehicles shows high neutral sentiment, signaling opportunities to convert it into positive. <br>
<h4>Emotional Drivers:</h4> 
• Fear is dominant in negative posts, often tied to concerns like recalls or reliability. <br>
• Trust dominates positive posts, linked to reliability and product quality. <br>
<h4>Competitor Insights:</h4> 
• Ford was historically discussed less than Stellantis and GM but recently surpassed both in post volume. <br>
• Stellantis leads in positive sentiment, but Ford shows opportunities to improve by converting neutral sentiment into positive. <br>

![Percent Positive, Negative, and Neutral - Ford + Competitor Reddit Posts](https://github.com/emilyschnepp/fordMCSocialListening/blob/14892cb1a2ee51ce835c1f05bda30386fd02fabe/visualizations/FMCPercPosNeutNeg.png)
<br>
The visualization above shows sentiment distribution across the Big 3. <br>

![Comparing Posts Over Time for Big 3 Companies](https://github.com/emilyschnepp/fordMCSocialListening/blob/14892cb1a2ee51ce835c1f05bda30386fd02fabe/visualizations/FMCCompareOverTime.png)
<br>
The visualization above highlights Ford's recent surge in Reddit mentions. <br>

![Trust and fear posts by subreddit](https://github.com/emilyschnepp/fordMCSocialListening/blob/14892cb1a2ee51ce835c1f05bda30386fd02fabe/visualizations/FMCTrustAndFear.png)
<br>
The visualization above compares trust and fear cross key subreddits. <br>

<h2>Future Work</h2> 
• Expand to other social media platforms. <br>
• Expand to other competitors. <br>
• Expand to include engagement metrics such as upvotes and comments. <br>
• Integrate additional information into the Prophet model to improve accuracy of model. <br>
• Build a real-time data pipeline. <br>
