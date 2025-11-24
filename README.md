# PHQ-9 Free-Text Depression Score Prediction (NLP)

This project uses **Natural Language Processing (NLP)** to predict **PHQ-9 depression scores** from free-text descriptions of symptoms.

Instead of using the usual multiple-choice PHQ-9 questionnaire (0–3 per item), this dataset contains **open-ended answers** to each of the 9 PHQ-9 questions, plus a final **PHQ-9 Score** and **Severity Level** for each person.  
The goal is to estimate the **numerical PHQ-9 score** directly from the text.

---

## 🧠 Problem Definition

- **Input:**  
  A combined free-text response to all 9 PHQ-9-style questions.

- **Output:**  
  A predicted **PHQ-9 score** (integer from 0 to 27).

- **Task type:**  
  **Supervised regression** (text → continuous score).

This can be seen as:  
> “Given how someone describes their mood, energy, sleep, and thoughts in their own words, how close can we get to their PHQ-9 depression score?”

---

## 🗂 Project Structure

```bash
phq9-nlp-depression-prediction/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   └── PHQ9_Student_Depression_Dataset_Updated.xlsx
│
├── notebooks/
│   └── 01_phq9_tfidf_regression.ipynb
│
└── models/
    └── phq9_random_forest_regressor.pkl   # (optional, if saved)
