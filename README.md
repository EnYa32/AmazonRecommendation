---
title: AmazonRecommendation
emoji: 🚀
colorFrom: red
colorTo: red
sdk: docker
app_port: 8501
tags:
- streamlit
pinned: false
short_description: Amazon Electronics product recommender
license: mit
---

# 🛒 Amazon Electronics Recommendation System

An Item-Based Collaborative Filtering project using Python, SciPy, and Cosine Similarity.

The goal of this project is to recommend similar electronic products based on user ratings and compare different recommendation approaches.

## 📊 Dataset

The project uses the Amazon Electronics Ratings dataset.

To reduce memory usage and processing time, I selected the most popular products and most active users.

- **Users:** 200,000
- **Products:** 4,000
- **Interactions:** 858,212
- **Matrix sparsity:** 99.89%

## 🧠 How It Works

1. Load and prepare the ratings data.
2. Select the most popular products and active users.
3. Create a sparse user-item matrix using SciPy.
4. Calculate cosine similarity between products.
5. Recommend products based on their similarity.
6. Improve recommendations by requiring at least five shared users.
7. Evaluate recommendation quality using Hit Rate@10.

The system calculates similarities when needed instead of storing a full item-item similarity matrix.

## 📈 Model Evaluation

I compared three recommendation approaches using an offline Leave-One-Out evaluation.

| Recommendation Approach | Hit Rate@10 |
|---|---:|
| Popularity-Based | 4.85% |
| Baseline Collaborative Filtering | 10.61% |
| **Improved Collaborative Filtering** | **10.95%** |

The improved model achieved the best results, with approximately **126% higher Hit Rate@10** compared to the popularity-based approach.

The results are based on two random train/test splits.

## 📉 Visualizations

The project includes:

- Product similarity distribution
- Shared user analysis
- User activity analysis
- Recommendation network visualization
- Model performance comparison

## 🛠️ Technologies

- Python
- Pandas and NumPy
- SciPy
- Scikit-learn
- Matplotlib and Seaborn
- Jupyter Notebook
- Streamlit

## 📁 Project Files

- `Notizbücher/AmazonRecommendation.ipynb` — Main notebook
- `requirements.txt` — Python dependencies

The notebook also contains code to export the sparse matrix and product mappings for use in a recommendation application.

## ▶️ How to Run

1. Clone or download the repository.
2. Install the required Python packages:

```bash
pip install -r requirements.txt
```

3. Download the Amazon Electronics Ratings dataset.
4. Update the dataset path in the notebook.
5. Open the notebook in Jupyter and run the cells in order.

## 🚀 Future Improvements

- Explore matrix factorization and other recommendation algorithms.
- Evaluate the system on additional datasets.
- Improve recommendation quality for products with few ratings.
- Build an interactive recommendation application.

## ✅ Conclusion

This project helped me understand how recommendation systems work with large and sparse datasets.

I learned how to build an item-based recommendation system, improve product similarity calculations, and evaluate different recommendation approaches.

The improved collaborative filtering model performed better than the baseline and popularity-based approaches in the offline evaluation.
