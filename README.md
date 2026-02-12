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

# 🛒 Amazon Electronics Recommender (Item-Based Collaborative Filtering)

This project builds a product recommendation system using the Amazon Electronics ratings dataset.

## ✅ Approach
- **Item-based collaborative filtering**
- Build a **sparse user–item matrix** using SciPy (CSR format)
- Compute **cosine similarity on-the-fly** to recommend similar products without storing a full item–item similarity matrix

## 🧠 Data Reduction
The original dataset is very large, so a reduced subset was used:
- `top_item = 4000` (most popular products)
- `top_user = 200000` (most active users)

This keeps the system scalable while preserving meaningful interactions.

## 📁 Files in this repo
Required files for the Streamlit app:
- `app.py`
- `R_sparse.pkl`
- `product_ids.pkl`
- `prod_to_idx.pkl`
- `requirements.txt`

## ▶️ Run locally
```bash
pip install -r requirements.txt
streamlit run app.py
