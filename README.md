# AT-T_Spam_Detector_NLP

![Accuracy](https://img.shields.io/badge/Accuracy-98%25-brightgreen?style=flat-square)
![F1-Score](https://img.shields.io/badge/F1--Score-93.2%25-blue?style=flat-square)

## 📌 Project Overview
This project aims to build an automated SMS spam detector for **AT&T** to protect users from constant exposure to fraudulent messages. Using a dataset of over 5,000 SMS, we developed a Deep Learning model capable of classifying messages as **Ham** (legitimate) or **Spam**.

## 🧠 Technical Strategy
### 1. Transfer Learning
Instead of training a model from scratch, we leveraged the power of **Google's Universal Sentence Encoder (USE)**. 
* **Input:** Raw or cleaned text sequences.
* **Embedding:** 512-dimensional vector representation of semantic meaning.
* **Architecture:** Dense layers with Dropout for regularization and a Sigmoid output for binary classification.

### 2. The Preprocessing Dilemma
A key finding of this project was the comparison between **Cleaned Text** (lowercase, no punctuation) and **Raw Text**. 
* **Result:** The model trained on **Raw Text** outperformed the cleaned version.
* **Insight:** Signals like CAPITAL LETTERS, currency symbols (£, $), and excessive punctuation (!!!) are crucial features that the USE model exploits to detect spam intent.

## 📊 Performance
The model achieves high reliability, specifically tuned to minimize **False Positives** to ensure no critical user messages are blocked.

| Metric | Score |
| :--- | :--- |
| **Accuracy** | ~98% |
| **F1-Score** | **93.2%** |



## 🛠️ Installation & Usage
1. Clone the repo: `git clone https://github.com/votre-nom/att-spam-detector.git`
2. Install dependencies: `pip install tensorflow tensorflow_hub pandas plotly scikit-learn`
3. Run the notebook: `jupyter notebook spam_detector.ipynb`

## 🚀 Future Evolutions
To stay ahead of spammers, the next steps include monitoring:
* **Homoglyph Attacks:** Visually identical characters from different alphabets.
* **Contextual Hijacking:** LLM-generated personalized spam.
* **Image-based Spam:** Text hidden within MMS images.

---
**Author:** [Ton Nom]  
**Project Context:** Data Science Deep Learning Project - AT&T Case Study
