# AI-Assignment-3
This is the project repository for AIPA Group 13 Assignment 3

## 👥 Group Members

| Name | Student ID |
|---|---|
| Keerthika Bottu | 25177698 |
| Shagun Sharma | 25200508 |
| Suhitha Motupalli | 25619709 |
| Vishal Chokalingam Nageshwar | 25526171 |
| Devvrat Charusmiti Joshi | 25657887 |
| Ayush Sharma | 25617592 |


## 📌 Project Overview

This project builds an AI-powered hybrid product recommendation system that goes beyond the only star ratings based recommendations. It uses two approaches. One is a Hybrid scoring system. A secondary RAG + LLM pipeline generates a natural language explanation using LLM.

## 🧠 AI Techniques Used

| Technique | Purpose |
|---|---|
| **TF-IDF** | Measures keyword similarity between user query and product text |
| **VADER Sentiment** | Scores customer reviews as Positive / Neutral / Negative |
| **FAISS** | Fast semantic vector search across all product embeddings |
| **RAG** | Grounds LLM responses in real retrieved products |
| **Logic-Based Filtering** | Hard rules for price, rating, and category constraints |

---

## 📂 Repository Structure

```
├── Assignment_3.ipynb       # Main notebook — full pipeline
├── README.md                # This file
└── evaluation_results.csv   # Model evaluation output (generated on run)
```

## 🗃️ Dataset

```
- **Source:** [Amazon Sales Dataset — Kaggle](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset)
- **Size:** 1,465 products
- **Fields used:** `product_name`, `category`, `discounted_price`, `actual_price`, `discount_percentage`, `rating`, `rating_count`, `about_product`, `review_title`, `review_content`
```

## ⚙️ System Workflow
```
User Query
    │
[1] Data Collection & Preprocessing
    │
[2] Text & Feature Preparation (TF-IDF + VADER)
    │
[3] Logic-Based Filtering
    │
[4] Hybrid Scoring (weighted fusion)
    │
[5] FAISS Semantic Retrieval
    │
[6] RAG + LLM Explanation
    │
Top-N Personalised Recommendations

```


### Prerequisites
```
- Python 3.8+
- Jupyter Notebook or Google Colab
```

### Steps to run

**1. Clone the repository**
```bash
git clone https://github.com/<your-repo-link>.git
cd <repo-folder>
```

**2. Open the notebook**
```bash
jupyter notebook Assignment_3.ipynb
```
Or upload to [Google Colab](https://colab.research.google.com/) and open there.

**3. Run all cells sequentially**

All dependencies are installed automatically in Cell 9:
```python
!pip install vaderSentiment sentence-transformers faiss-cpu transformers networkx -q
