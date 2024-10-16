# Data Mining Project

## Table of Contents

1. [Preprocessing](#preprocessing)
   - [Import Prerequisites](#import-prerequisites)
   - [Load Files](#load-files)
   - [Merge Datasets per Year](#merge-datasets-per-year)
   - [2019 Post Processing](#2019-post-processing)
   - [2023 Post Processing](#2023-post-processing)
2. [Null Values](#null-values)
   - [Null Values in 2019](#null-values-in-2019)
   - [Null Values in 2023](#null-values-in-2023)
3. [Clean up](#clean-up)
   - [Cleanup 2019](#cleanup-2019)
   - [Cleanup 2023](#cleanup-2023)
4. [Price to Float](#price-to-float)
5. [Part 1 - Problems](#part-1-problems)
   - [1.1 Most Frequent Room Type](#11-most-frequent-room-type)
   - [1.3 Top 5 Neighbourhoods with Most Reviews](#13-top-5-neighbourhoods-with-most-reviews)
   - [1.4 Neighbourhood with Most Entries](#14-neighbourhood-with-most-entries)
   - [1.5 Entities per Month and per Neighbourhood](#15-entities-per-month-and-per-neighbourhood)
   - [1.6 Histogram of Neighbourhood](#16-histogram-of-neighbourhood)
   - [1.7 Most Frequent Room Type per Neighbourhood](#17-most-frequent-room-type-per-neighbourhood)
   - [1.8 Most Expensive Room Type](#18-most-expensive-room-type)
   - [1.9 Map with Mean Coordinates](#19-map-with-mean-coordinates)
   - [1.10 Wordcloud for Neighbourhood, Transit, Description, Last Review](#110-wordcloud-for-neighbourhood-transit-description-last-review)
   - [1.11 Distribution of Simplified Amenities Categories](#111-distribution-of-simplified-amenities-categories)
   - [1.12 Mean for 2 People Room per Neighbourhood](#112-mean-for-2-people-room-per-neighbourhood)
   - [1.13 Three Additional Questions for Athens](#113-three-additional-questions-for-athens)
   - [1.14 Top 10 Hosts with Most Listings](#114-top-10-hosts-with-most-listings)
   - [1.15 Conclusions](#115-conclusions)
6. [Part 2 - Recommendation System](#part-2-recommendation-system)
   - [TF-IDF Vectorization](#tf-idf-vectorization)
   - [Cosine Similarity](#cosine-similarity)
   - [Recommendation System](#recommendation-system)

## Preprocessing

### Import Prerequisites
In this section, necessary libraries and tools used throughout the notebook are imported. These include popular data manipulation libraries like pandas, data visualization tools such as matplotlib and seaborn, and NLP (natural language processing) tools like `nltk` for text processing. Additionally, stopwords from the `nltk` library are downloaded to assist in the text-cleaning process later on.

### Load Files
Here, the datasets from the Airbnb listings in different months of 2019 and 2023 are loaded into memory. The CSV files for the respective years are read and printed to understand the structure (rows and columns) of each dataset.

### Merge Datasets per Year
The individual monthly datasets for each year (2019 and 2023) are merged into single datasets. This allows easier data processing, ensuring that all listings from various months in a year are available in one unified dataset.

### 2019 Post Processing
This segment handles post-processing of the 2019 dataset. It includes steps like handling missing values, feature extraction, and data cleaning to prepare the dataset for further analysis. Each column in the dataset is examined, and irrelevant data is either removed or transformed into a useful format.

### 2023 Post Processing
Similar to the 2019 post-processing step, this section involves cleaning and extracting important features from the 2023 dataset. Data is cleaned by addressing missing values and performing operations such as data normalization or transformation for consistency.

## Null Values

### Null Values in 2019
In this section, the notebook examines the 2019 dataset for missing values. The results help identify which columns have null or missing data, allowing the user to decide how to handle them (e.g., by filling, removing, or ignoring them).

### Null Values in 2023
Similar to the 2019 dataset, the 2023 dataset is examined for null values. The missing data is identified, and this step provides insight into which columns need further attention.

## Clean up

### Cleanup 2019
This step involves the actual cleaning of the 2019 dataset. Missing or erroneous values are handled by either imputing, filling with default values, or removing unnecessary columns. The goal is to create a clean, ready-to-analyze dataset.

### Cleanup 2023
As with 2019, the 2023 dataset undergoes a similar cleaning process to remove or handle missing values, prepare the data, and ensure that all features are in the correct format for further analysis.

## Price to Float
The price column in both datasets (2019 and 2023) is stored as a string with symbols (e.g., dollar signs). In this step, the price is converted into a numeric format, specifically a floating-point number, so that mathematical operations and comparisons can be performed.

## Part 1 - Problems

### 1.1 Most Frequent Room Type
This section identifies the most common or frequent room type in both the 2019 and 2023 datasets. The analysis gives insight into which type of accommodation is most popular.

### 1.3 Top 5 Neighbourhoods with Most Reviews
In this step, the top 5 neighborhoods that received the most reviews are identified. This helps in understanding the most active or popular neighborhoods in terms of user feedback and interaction.

### 1.4 Neighbourhood with Most Entries
This section finds the neighborhood that has the highest number of listings. It can indicate the area with the most rental activity or popularity.

### 1.5 Entities per Month and per Neighbourhood
The data is analyzed to check how many entities (listings) are created or active per month and per neighborhood. This can give an idea of seasonal trends or neighborhood popularity over time.

### 1.6 Histogram of Neighbourhood
A histogram is generated to visualize the distribution of listings across different neighborhoods. This visualization helps in understanding how the listings are spread geographically.

### 1.7 Most Frequent Room Type per Neighbourhood
This analysis dives deeper by identifying the most common room type in each neighborhood. It provides a breakdown of the preferred types of accommodations across different areas.

### 1.8 Most Expensive Room Type
This section identifies which room type is the most expensive in terms of listing price. It offers insight into the high-end market and which types of accommodations attract the highest prices.

### 1.9 Map with Mean Coordinates
A map is generated using the mean coordinates of listings in each neighborhood, providing a geographical overview of where listings are concentrated.

### 1.10 Wordcloud for Neighbourhood, Transit, Description, Last Review
Wordclouds are generated for textual data in the datasets, such as neighborhood descriptions, transit information, and reviews. This helps visualize the most common words or phrases associated with these categories.

### 1.11 Distribution of Simplified Amenities Categories
This section looks at the amenities offered by listings, grouping them into simplified categories, and analyzing the distribution. It provides an understanding of which amenities are most frequently offered.

### 1.12 Mean for 2 People Room per Neighbourhood
Here, the mean price for a two-person room in each neighborhood is calculated and analyzed, giving insight into pricing patterns across areas.

### 1.13 Three Additional Questions for Athens
This part of the notebook explores three specific questions about listings in Athens:
1. How does the number of reviews correlate with review scores?
2. Do hosts with verified identities and profile pictures receive better ratings or more bookings?
3. What is the relationship between the instant bookable feature and the review score?

### 1.14 Top 10 Hosts with Most Listings
The top 10 hosts with the most listings are identified. This analysis helps in understanding the most active or influential hosts in the market.

### 1.15 Conclusions
This section summarizes the conclusions drawn from the data mining process, based on the insights generated from the analysis of both 2019 and 2023 datasets.

## Part 2 - Recommendation System

### TF-IDF Vectorization
In this section, the text data (e.g., reviews, descriptions) is processed using TF-IDF vectorization to represent textual information in numerical format. This is essential for further analysis, especially for calculating similarities between texts.

### Cosine Similarity
Once the text data is vectorized, cosine similarity is used to calculate the similarity between different texts. This method helps in finding similar listings based on textual information.

### Recommendation System
Using the vectorized data and similarity measures, a recommendation system is built. The system suggests listings to users based on similarities in features or textual descriptions.
