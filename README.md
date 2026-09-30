# Collaborative Filtering Engine (CF-Engine)

This repository contains a collaborative filtering recommender system built entirely from scratch, developed for the Introduction to Machine Learning course at Alexandria University[cite: 1, 2]. 

The engine predicts user ratings for movies by identifying patterns in a ratings matrix, implementing both user-based and item-based approaches[cite: 1]. To analyze how different distance metrics behave with rating scale offsets and matrix sparsity, the system evaluates recommendations using three distinct similarity calculations[cite: 1, 2].

## Core Features

*   **Custom Similarity Metrics:** Implements Euclidean distance, Cosine similarity, and Pearson correlation from first principles without external machine learning libraries[cite: 1, 2, 3].
*   **Sparsity Handling:** Calculates similarity strictly over co-rated items to prevent missing data from silently skewing predictions[cite: 2].
*   **Dual-Direction Filtering:** 
    *   *User-Based CF:* Predicts ratings via a similarity-weighted average of the k-nearest users[cite: 1, 2].
    *   *Item-Based CF:* Predicts ratings via a similarity-weighted average of the k-nearest items[cite: 1, 3].
*   **Quantitative Evaluation:** Features a custom train/test split mechanism that holds out 20% of each user's ratings to evaluate Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE)[cite: 4].

## Tech Stack

*   **Language:** Python 3.9+[cite: 3]
*   **Libraries:** `pandas` and `numpy`[cite: 3]
*   *Note: Scikit-learn, Surprise, and other algorithmic recommender libraries are strictly excluded by design to focus on algorithm mechanics[cite: 3, 5].*

## Dataset

This project uses the standard **MovieLens latest-small** dataset, containing approximately 100,000 ratings from 600 users across 9,000 movies[cite: 3]. 

**Data Setup:**
1. Download the dataset from [GroupLens Research](https://files.grouplens.org/datasets/movielens/ml-latest-small.zip)[cite: 3].
2. Extract the archive and place `ratings.csv` and `movies.csv` into a directory named `data/` at the root of this project[cite: 3].

## Usage & Execution

The entire pipeline is contained within a Jupyter Notebook[cite: 3]. 

1. Ensure the `data/` folder is populated with the MovieLens `.csv` files[cite: 3].
2. Run the notebook cells sequentially to load the matrix, handle missing values, and execute the grid search[cite: 3, 4].

## Evaluation Results

| Method | Similarity Metric | K-Neighbors | RMSE | MAE |
| :--- | :--- | :--- | :--- | :--- |
| User-Based | Pearson | 20 | TBD | TBD |
| Item-Based | Cosine | 50 | TBD | TBD |

## Contributors

*   **Mohamed** ([GitHub Profile Link])
*   **Omar** ([GitHub Profile Link])
*   **Aly** ([GitHub Profile Link]) 
