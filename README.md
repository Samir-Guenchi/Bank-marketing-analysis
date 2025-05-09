# 📊 Multi-Model Evaluation on Imbalanced Dataset

This project evaluates multiple classification models on a dataset with a strong class imbalance. The goal was to identify the model that best balances performance metrics (precision, recall, F1-score) after applying SMOTE to the training data.

---

## 🧠 Models Compared

| Model           | Accuracy | Precision | Recall | F1-score |
|----------------|----------|-----------|--------|----------|
| Decision Tree  | 0.877    | 0.479     | 0.591  | **0.529** |
| Random Forest  | **0.903**| **0.653** | 0.358  | 0.463    |
| KNN            | 0.884    | 0.506     | 0.240  | 0.326    |
| Naive Bayes    | 0.835    | 0.361     | 0.539  | 0.432    |
| SVM            | 0.900    | 0.618     | 0.389  | 0.478    |
| Neural Network | 0.884    | 0.506     | 0.516  | 0.511    |

> 📈 **Model comparison chart** available as: `model_comparison.png`

---

## ⚖️ Handling Imbalanced Data

- **Initial Class Distribution:**
  - Negative (False): 88.3%
  - Positive (True): 11.7%
  - Imbalance ratio: 7.55:1

- **Balancing Technique:**  
  SMOTE (Synthetic Minority Oversampling Technique) was applied to the **training data only** to create a more balanced representation of both classes.

- **Dataset Breakdown:**
  - Training data before SMOTE: 36,168 samples
  - Training data after SMOTE: 63,874 samples
  - Test data (unchanged): 9,043 samples

---

## 🏆 Best Model: Decision Tree

While Random Forest had the highest **accuracy (0.903)** and **precision (0.653)**, the **Decision Tree** was selected as the best overall model due to its **higher F1-score (0.529)** and **recall (0.591)** — making it better suited for imbalanced data where detecting positive cases is crucial.

---

## 🔑 Top 3 Important Features (by Decision Tree)

1. `duration` – 0.278  
2. `poutcome_success` – 0.096  
3. `campaign` – 0.063

---

## 📁 Files Included

- `model_comparison.png` – Visual summary of model performance  
- `README.md` – Project documentation  
- `notebook.ipynb` or `model_evaluation.py` – (optional: add your code file name here)

---

## 🧪 Notes

- Metrics were calculated using the test set **with original imbalance** to reflect realistic performance.
- Emphasis was placed on **F1-score and recall**, which are more meaningful in real-world applications with minority class importance.

---

## 📬 Contact

For questions or collaboration, feel free to reach out via [GitHub Issues](https://github.com/Samir-Guenchi).

