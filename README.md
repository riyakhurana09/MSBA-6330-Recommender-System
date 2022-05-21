# MSBA-6330-Recommender-System

This project repository is created in partial fulfillment of the requirements for the Big Data Analytics course offered by the Master of Science in Business Analytics program at the Carlson School of Management, University of Minnesota.

Team 3 - MSBA Class of 2022 - Trends Marketplace Project (Big Data Analytics)

## Executive Summary
Recommendation systems are used by many large companies to enhance the quality of their services by understanding the taste of the customers. The main audience of our recommendation system is companies that want to generate additional business / revenue by strategically recommending products to customers based on their tastes and ratings given to similar products.

To provide recommendations based on item ratings, we will use a technique called Collaborative Filtering. The basic idea is the use the similarity between books to make predictions for a given user (Song, 2022). Our model was built using k-Nearest Neighbors (kNN) methods, which uses the ratings of books to calculate the distance between a specific book and all other books in the dataset (Liao, 2018). The output will return a list of recommended books based on a predicted rating in descending order.

## Data Source
Books: Over 1.1M different ratings of books. The dataset includes three tables:
1. Books (ISBN, Title, Author, Year, Publisher)
2. Ratings (ISBN, UserId, Ratings)
3. Users (Age)

Dataset: https://www.kaggle.com/datasets/somnambwl/bookcrossing-dataset

## Recommendation System Video
The video below will provide an introduction to our book recommendation system. We’ll discuss how the recommendation system works and how the system provides recommendations to users.

[Group 3 Recommendation System Video](https://youtu.be/lq3Jw0CcNqY)

## Recommendation System Flyer
[Group 3 Flyer](/flyer.pdf)

## Technology Used
We utilized the technologies below to implement our book recommendation system:
- Kaggle: Provided book data source
- Amazon S3: Used to store our dataset of 1.1M different ratings of books
- Amazon SageMaker: Used to implement / run our recommendation system

## Business Use Cases
Any company that wants to cross-sell items and / or increase customer satisfaction can use a recommendation system like the one we built. A recommendation system is very valuable in the retail industry, but is also widely used today with streaming services. Here are a couple specific business use cases:
1. Target (Retail) - cross sell similar items through top recommendations
2. Spotify (Streaming) - recommend additional songs like a recently played song

## Limitations
With the limited computational resources available to us, we were unable to run our book recommendation system on the entire dataset. We successfully loaded all data into Amazon S3 and built the model with Jupyter Notebook in SageMaker; however, we pulled a subset of the data to test that our model performed as expected. The recommendation model is fully operational and can be implemented for any business use cases that have the appropriate computational resources. Another limitation is the number of recommendations provided to a user. It’s not feasible to provide all book recommendations to a user; therefore, a business decision needs to be made regarding the top number of books, for example 20 or 30, provided to a specific user. Third, evaluating the effectiveness of any recommendation system is challenging due to underlying preference assumptions. Finally, finding similar products is difficult for niche books.

## Resources
Our team used the following websites / resources to assist with our recommendation system project:

1. https://aws.amazon.com/blogs/machine-learning/building-a-customized-recommender-system-in-amazon-sagemaker/
2. https://www.kaggle.com/code/philippsp/book-recommender-collaborative-filtering-shiny
3. https://towardsdatascience.com/prototyping-a-recommender-system-step-by-step-part-1-knn-item-based-collaborative-filtering-637969614ea
