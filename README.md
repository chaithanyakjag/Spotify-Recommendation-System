# Spotify-Recommendation-System

## Introduction
This recommendation system is designed to help users discover songs similar to their existing playlist preferences. The system analyzes song attributes (e.g., genres, release dates) and creates feature vectors to represent each song. It then uses **cosine similarity** to compare these vectors with the user's playlist and recommends songs that have the highest similarity scores. The entire system is built to handle large datasets efficiently, utilizing techniques like **batch processing** and **feature normalization** to ensure performance and scalability.

## Project Overview
- **Type:** Content-Based Recommendation System
- **Techniques:** TF-IDF, One-Hot Encoding, Feature Vectors, Cosine Similarity
- **Objective:** To suggest new songs similar to those in a user's playlist by analyzing song attributes.
- **Dataset:** A dataset containing song metadata (e.g., genres, release dates, artists).

## Data Preparation
1. **Data Loading:** 
   - Load the Spotify song data into a pandas DataFrame.
2. **Data Cleaning:**
   - Remove duplicates and handle missing values.
3. **One-Hot Encoding:**
   - Convert categorical features (e.g., genres, explicit content) into numerical vectors using one-hot encoding.

## Feature Engineering
1. **TF-IDF Vectorization:**
   - Apply TF-IDF to the genres column to convert text data into numerical vectors.
   - This helps represent the relevance of each genre for a song.
2. **Creating Feature Vectors:**
   - Combine TF-IDF vectors, one-hot encoded vectors, and other song attributes into a single feature vector for each song.
3. **Normalization:**
   - Normalize the numerical features to ensure they have the same scale.
  
## Model Building
1. **Cosine Similarity:**
   - Compute cosine similarity between the user's playlist vector and all song vectors in the dataset.
   - This measures the similarity between songs based on their feature vectors.
2. **Content-Based Filtering:**
   - Recommend songs based on their similarity scores, focusing on songs that are most similar to the user’s existing preferences.

## Recommendations Generation
1. **Batch Processing:**
   - To handle large datasets, process recommendations in batches to optimize memory usage.
2. **Top-K Recommendations:**
   - Select the top-K songs with the highest cosine similarity scores as recommendations.
