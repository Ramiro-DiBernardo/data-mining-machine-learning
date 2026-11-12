# 🧠 Data Mining & Machine Learning

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-154F5B?style=for-the-badge)

Notebooks from the **Data Mining** course of my **Associate Degree in Data Science and Artificial Intelligence (ISTEA)**: from exploratory analysis and preprocessing to supervised and unsupervised learning, NLP and convolutional neural networks.

*Notebooks, comments and outputs are in Spanish.*

## ⭐ Featured: neighborhood clustering on Boston Housing

[`01-boston-housing-clustering`](01-boston-housing-clustering/boston_housing_clustering.ipynb) is my individual work for the course's second exam.

| Step | What it does |
|---|---|
| Scaling | `StandardScaler`, so that variables measured in hundreds (`TAX`, `B`) don't dominate the distances |
| K-Means | 3 clusters (`random_state=42`) and a profile of each one in the original units |
| Elbow method | Inertia for k = 1…10. The curve bends between k = 2 and k = 3 |
| PCA | Reduction to 3 principal components, loadings and a 3D plot with projected centroids |
| Silhouette | 0.234 for k = 3. The best score is k = 2 (0.350); k = 3 trades some separation for an interpretable middle group |
| NLP extra | Stop-word removal with NLTK |

**Clusters found:**
- **Affluent residential** (146 homes): low crime, larger homes, highest median value (31.4k).
- **Urban / industrial** (156 homes): high crime, industry and pollution, lowest median value (16.2k).
- **Intermediate** (204 homes): median value 21.1k.

> ⚠️ **About the dataset:** Boston Housing (1978) includes the variable `B`, derived from the proportion of Black residents per town. For that reason scikit-learn removed the dataset in version 1.2. It is used here only because the exam required it. In a real analysis that variable should be dropped, or an alternative such as *California Housing* used.

## 📚 Coursework

These notebooks were built **in class together with the teacher**, and are shared with the teacher's permission.

| # | Topic | Notebooks | Techniques |
|---|---|---|---|
| 02 | [EDA & preprocessing](coursework/02-eda-and-preprocessing) | `eda_preprocessing` | Descriptive statistics, ordinal vs. nominal encoding (`LabelEncoder`, `OneHotEncoder`), `MinMaxScaler` |
| 03 | [Statistics](coursework/03-statistics) | `statistics` | Descriptive statistics, correlation matrix |
| 04 | [HR attrition EDA](coursework/04-hr-attrition-eda) | `hr_attrition_eda` | EDA on an HR dataset, transformations, encoding and scaling |
| 05 | [Supervised learning](coursework/05-supervised-learning) | `supervised_learning`, `random_forest` | Decision trees (how to read Gini, samples and leaves), bootstrapping, random forest, confusion matrix |
| 06 | [Unsupervised learning](coursework/06-unsupervised-learning) | `unsupervised_learning`, `pca` | K-Means, DBSCAN, PCA |
| 07 | [NLP: sarcasm detection](coursework/07-nlp-sarcasm-detection) | `nlp_sarcasm` | Text EDA, stemming, lemmatization, `CountVectorizer`, random forest classifier |
| 08 | [Neural networks](coursework/08-neural-networks) | `cnn_cifar10`, `xray_pneumonia_cnn` | Dense networks vs. CNNs on CIFAR-10, pneumonia detection on chest X-rays |

Some notebooks were run in Google Colab and read datasets from Drive (insurance, HR, X-rays), so those files are not in the repo. Small datasets are included in each `data/` folder.

## ⚙️ Requirements

```bash
pip install -r requirements.txt
```
