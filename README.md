# Molson-Coors-Recommender-System

🧠 Project Overview

This project builds a recommender system to encourage Budweiser customers to try Molson Coors products, using real retail transaction data from the ACSE grocery chain. The dataset captures actual customer behavior across millions of purchases, spanning thousands of products, stores, and time periods — making it ideal for testing real-world recommendation strategies

📊 Dataset & Tools

- Worked with a 1B+ row transaction dataset (not uploaded due to size). This was converted to parquet format for size optimization
- Used DuckDB and GCP BigQuery for efficient SQL querying
- Performed 10% stratified sampling, validated with KS and Chi-Square tests to ensure accurate statistical depiction of original dataset.

🎯 Goal

Target Budweiser buyers and recommend Molson products to increase cross-brand sales.

🧪 Baseline

19.07% of Budweiser customers already purchased Molson — this served as the baseline conversion rate

We used this to measure lift for each model

🤖 Models Tested

Popularity-Based (best performance)

Item-Based & User-Based CF

Content-Based (TF-IDF)

ALS (Matrix Factorization)

BPR (Bayesian Personalized Ranking)

Naive Bayes Classifier

🏆 Results

- Popularity model achieved a 52% lift over baseline

- BPR showed potential for long-term personalization

- Other models struggled due to matrix sparsity and low co-purchase signals
