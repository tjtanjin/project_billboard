# Project Billboard Model
Project billboard is one of the projects initiated by UpCode Academy for its students to gain more exposure and experience. The objective of this project is to produce a model that is capable of predicting the potential of a song to be a billboard hit.

Note: The project billboard model repository contains work strictly pertaining to the training of our prediction models. For the repository that contains our work on the frontend and API, please refer to the project billboard api repository: https://github.com/tjtanjin/project_billboard_api

# Timeline
### 2nd April 2019
2nd April marks the start of our project. With the details of the project unveiled, we began to discuss about the approach and resources that we can use. Spotify's API looked promising for extracting song features as we moved into webscraping the billboard chart for top songs of every week!

### 18th April 2019
We held our very first meeting at Starbucks where we finalized on a couple of resources to use and allocated various tasks. Spotify was confirmed as our main source for collecting song features and it's popularity scores used to label our song data. Specifically, a score of 70 and above will be classified as a hit while anything below will be classified as a miss. This github repository was also created for ease of collaborating on the codes for the project.

### 29th April 2019
We have scraped songs from spotify as well and at this point, hold 5 years worth of top 10000 songs dataset from 2014-2018. To balance the dataset, we randomly dropped the "miss" labeled songs until the number of hits and misses are equal. We tested a couple of simple algorithms for hit/miss prediction as we continued to scrape the songs from the billboard chart.

### 6th May 2019
Our models proved decent (60%-70% accuracy) on spotify's labels but performed worst when the billboard label was used. After some analysis using f1_score and the confusion matrix from sklearn, we realized that the problem was likely with our imbalanced dataset (previously balanced based on spotify label). After rebalancing the dataset around billboard labels instead, we added more songs from the years 2009-2013.

### 11th May 2019
At this point, our model accuracy on the billboard label has increased to the range of 60%-70% and is decent in making most predictions. However, the dataset used to train our model contained only about 3000 songs (the small size is partially due to an inefficient approach we took to collecting the songs). Despite the closing of our project, we will still be continuously improving our models and increasing the datasets. Do check in on updates!

# Type of Prediction Models
Our team mainly experiemented with the 3 types of models as below. The final mean accuracies of these models is in brackets:
- Logistic Regression Model (65.2%)
- K Nearest Neighbours Model (61.2%)
- XGBoost Model (68.7%)

# Upcoming Work
- Reverse the song collection approach to scrape from billboard first before scraping from spotify (utilizing every single billboard hit will increase our current dataset).
- Retrieve songs from years 2000-2008 as well, effectively increasing our range of songs to 19 years.
- Retrain song models on a much larger dataset.