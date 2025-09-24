***Recommender System for a Grocery Chain***

**Project Overview**

This project builds a recommender system to encourage Budweiser customers to try Molson Coors products, using real retail transaction data from the ACSE grocery chain. The dataset captures actual customer behavior across millions of purchases, spanning thousands of products, stores, and time periods — making it ideal for testing real-world recommendation strategies.

**Dataset & Tools**

- Data: a 1B+ row transaction dataset (not uploaded due to size). This was converted to parquet format for query optimization
- Tools: DuckDB efficient SQL querying  and GCP BigQuery for querying and storing the large dataset

**Project Goal**

The recomender system aims to target Budweiser buyers and recommend Molson products to increase cross-brand sales.

**Data Processing**

- Performed 10% stratified sampling, validated with KS (Kolmogorov–Smirnov Test) and Chi-Square tests to ensure accurate statistical depiction of original dataset.
  - The KS test: compares two distributions to see if they are different. The test checks for the distance between two CDF curves and calculates the p-value.
- 19.07% of Budweiser customers already purchased Molson — this served as the baseline conversion rate. This was used to measure lift for each model.
  -  A lift > 1 means the model is not randomly guessing.
  -  Lift = model success rate ÷ baseline success rate

**Recomender Systems**

- Popularity-Based (best performance)

- Item-Based & User-Based CF

- Content-Based (TF-IDF)

- ALS (Matrix Factorization)

- BPR (Bayesian Personalized Ranking)

**Results**

- The popularity model achieved a 52% lift over the baseline. 

- BPR showed potential for long-term personalization.

- Other models struggled due to matrix sparsity and low co-purchase signals.
