# WeRateDogs Twitter Data Analysis

## Project Overview

This project involves data wrangling and analysis of the WeRateDogs Twitter account. The goal is to gather, assess, clean, and analyze the data to extract meaningful insights about dog ratings and tweet engagement.

## Datasets

### 1. Tweets Archive
- **Source:** Provided by the instructor
- **Format:** CSV
- **Contents:** Enhanced tweets archive of the 'WeRateDogs' Twitter page, including tweet ID, text, source, URL, timestamp, and more.
- **Size:** 2356 rows, 17 columns
- **DataFrame:** `df_archive`

### 2. Image Predictions
- **Source:** Provided by the instructor
- **Format:** TSV
- **Contents:** Predictions about the breed of the dog in each tweet's images, confidence levels, and whether each prediction is a dog or not.
- **Size:** 2075 rows
- **DataFrame:** `df_images`

### 3. Tweet Engagement
- **Source:** Provided by the instructor
- **Format:** JSON
- **Contents:** Retweet count and likes count for each tweet.
- **DataFrame:** `likes_df`

## Assessing the Datasets

All three dataframes were assessed visually and programmatically to understand the data and identify quality and tidiness issues.

### Quality Issues
- Rating denominator column in the Twitter archive has values other than 10.
- Some tweets in the Twitter archive dataframe are duplicates.
- Missing values in the name column are represented as 'none'.
- Timestamp column is in string data type.
- Inaccurate values in the name column (e.g., 'a').
- 'retweeted_status_timestamp' column is in string data type instead of datetime.
- 'None' values in doggo, pupper, floofer, and puppo columns are inaccurate representations.
- Some column names in the image prediction table are not descriptive enough.

### Tidiness Issues
- Dog stage is represented in multiple columns in the archive dataset.
- Relevant columns from all tables should be merged to form a single table.

## Cleaning the Data
[Check out the data cleaning notebook here](https://github.com/maleek004/Udacity_data_analysis_nanodegree_projects/blob/main/project_2_data_wrangling/wrangle_act.ipynb)

- Copies of all three dataframes were made to preserve the original data. Cleaning was performed on the copies, addressing quality issues first, followed by tidiness issues.

### Quality Cleaning
- Used `pd.to_datetime()`, `str.replace()`, and `rename()` functions to resolve issues.

### Tidiness Cleaning
- Used `df.drop()`, `+` operator to concatenate columns, and `merge()` to merge all three tables together.

## Final Result

After cleaning, a master dataset was created containing 1994 tweets in 13 columns, holding all needed information about each tweet, dog breed prediction, dog ranking, and bio.

[Check out the data cleaning reports notebook here](https://github.com/maleek004/Udacity_data_analysis_nanodegree_projects/blob/main/project_2_data_wrangling/wrangle_report.ipynb)

## Insights from the WeRateDogs Twitter Page Analysis

Historical data about dog ratings tweets from the 'WeRateDogs' Twitter page were gathered and cleaned. An analysis was then run on the wrangled data, producing the following insights:

### Insight 1
The most tweeted about and most popular dog breeds are Golden Retriever, Labrador Retriever, Pembroke, and Chihuahua. These breeds were also the most liked, retweeted, and highly rated.

### Insight 2
The most engaging tweets were posted between 11 PM to 1 AM and 3 PM to 6 PM. 77% of the 100 most liked tweets were tweeted during these hours.

### Insight 3
The dog stage 'doggo' is the most common among the most liked tweets.

### Insight 4
There is a positive correlation between tweet likes count and retweet count.

### Insight 5
There is a slight positive correlation between tweet likes and rating.

[Check out the final insights notebook here](https://github.com/maleek004/Udacity_data_analysis_nanodegree_projects/blob/main/project_2_data_wrangling/act_report.ipynb)

## Summary
Golden Retrievers are the favorite dog breeds, followed by Labrador Retriever, Samoyed, and Pembroke in the doggo stage. The best times to tweet for engagement are around midnight or 4 PM. The dog with the best performing tweet in terms of likes, retweets, and rating was a black and white standard poodle named BO in the doggo stage, tweeted in January 2017 at about 2 AM, with over 95,000 likes, over 42,000 retweets, and a rating of 14/10.

![BO the dog](https://github.com/user-attachments/assets/c6a0abe5-fde4-4fc8-85ac-b8ea1e119d3b)

