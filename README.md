# beer-recommender-system

Companies across industries have always relied on customer sentiment and perceptions to make key decisions on marketing strategy or product alterations. In this project, I scraped ~10K reviews from an online beer review forum to formulate and devise a beer recommendation system that can help consumers identify new beers that resonate closely with their preferred beer brands.

There were 3 major phases in this exercise - 

1) Data Scraping - Scraped reviews from the popular beer forum - "Beer Advocate" using Selenium. To have meaningful data, I only considered brands that had a minimum of 50 reviews.

2) Data Pre-Processing and EDA - Since I was working with user generated data, some basic data cleaning was needed to structure the data to perform subsequent analysis; some of the key steps here were :
- Removing stop words
- Removing punctuations
- Using word embeddings

Additionally, eye-balling the data helped me identify key attributes that the users used to describe different beers; so I grouped various adjectives into buckets suchs as Hoppy, Fruity, Malty, etc.

I also performed a word frequency analysis to club similar words together and then performed a LIFT analysis to identify to what attributes is each brand identified with by customers.

3) Building Recommendation System - I created a composite scoring index for each brand using - 

- Similarity Score
- VADER Sentiment Score

The Similarity score was calculated using 2 approaches - (i) Bag of Words (ii) Spacy Word Embeddings. the main reason for following these 2 approaches is that each method can be more relevant in different situations. For instance, when a more generalized meaning needs to be captured Words Embeddings is the ideal route of action but when exact matches are needed then the Bag of Words approach needs to prioritized.

