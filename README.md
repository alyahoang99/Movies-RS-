# Overview

This project is for self-learning as non-technical product manager to understand  different recommendation system approaches for movies/series recommendation, aiming to enhance user experience and engagement on streaming platforms. By understanding these models, a product manager can make informed decisions about recommendation strategies that balance technical feasibility with business goals.

Dataset

The dataset consists of two main tables:

Movies Data: Contains movie titles, genres, and release years.

User Interaction Data: Includes user IDs, movie ratings, timestamps, and contextual information (daytime, weekend activity).

Recommendation Approaches

1. Content-Based Filtering

Approach: Recommends movies similar to those a user has previously liked by analyzing features such as genres.

Implementation: Uses cosine similarity between movie feature vectors.

Interpretation: Works well for new users with limited interaction data but can lead to a "filter bubble" where users only see similar types of content.

2. Collaborative Filtering (Matrix Factorization)

Approach: Predicts user preferences based on interactions of similar users.

Implementation: Uses Singular Value Decomposition (SVD) or alternative matrix factorization techniques.

Interpretation: Effective in capturing latent factors influencing user preferences, but struggles with cold-start users (new users with no history).

3. Deep Learning (Neural Networks)

Approach: Learns complex patterns in user behavior and content interactions.

Implementation: Uses TensorFlow/Keras-based deep learning models to predict user ratings.

Interpretation: Can capture non-linear relationships and contextual dependencies but requires large-scale data and computational power.

4. Hybrid Approach

Approach: Combines content-based and collaborative filtering to leverage the strengths of both.

Implementation: Merges similarity-based filtering with matrix factorization or deep learning models.

Interpretation: Helps mitigate cold-start issues and improves recommendation diversity.

Hybrid Model Metrics and Interpretation

1. Accuracy Metrics

RMSE (Root Mean Square Error) / MAE (Mean Absolute Error): Lower values indicate better prediction accuracy for user ratings. If RMSE is significantly lower than standalone models, the hybrid model effectively integrates both approaches.

Precision & Recall: High precision ensures high-quality suggestions, while high recall means the model surfaces relevant recommendations effectively.

2. Ranking Metrics

NDCG (Normalized Discounted Cumulative Gain): Higher scores indicate that relevant recommendations are ranked better, improving user satisfaction.

Mean Reciprocal Rank (MRR): Higher MRR suggests the first relevant recommendation appears earlier, leading to better engagement.

3. Diversity & Novelty Metrics

Intra-list Similarity: Lower values indicate diverse recommendations, reducing filter bubbles.

Serendipity & Novelty: A well-performing hybrid model balances personalization with unexpected but relevant discoveries, enhancing engagement.

4. Business & User Engagement Metrics

Click-through Rate (CTR) & Conversion Rate: Higher CTR suggests better alignment with user preferences, leading to increased interactions.

Business Insights

Each approach provides different trade-offs:

Content-Based Filtering: Ensures personalized recommendations but may lack diversity.

Collaborative Filtering: Enhances discovery but struggles with new users.

Deep Learning: Captures richer user behavior but requires significant data.

Hybrid Models: Offer a balanced approach for scalable recommendation systems.

How to Run

Install dependencies: pip install pandas numpy scikit-learn tensorflow

Load the dataset (data_movies.xlsx).

Run each section of the notebook sequentially.

Evaluate the model performance using defined success metrics.
