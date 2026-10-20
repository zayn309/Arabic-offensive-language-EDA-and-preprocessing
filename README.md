# Arabic Offensive Language & Hate Speech: Exploratory Data Analysis & Preprocessing

This repository contains the Exploratory Data Analysis (EDA) and data preprocessing pipeline for an Arabic social media dataset focusing on hate speech, vulgarity, and offensive language detection across multiple platforms (Twitter, Facebook, YouTube).

---

## 📋 Project Overview

Social media content moderation in Arabic presents unique challenges due to dialectal variations, code-switching, and cultural nuances. This project processes an annotated dataset of **4,000 Arabic social media comments** to uncover structural patterns, class imbalances, and linguistic traits across platforms.

### Key Objectives:
* **Data Cleansing & Validation:** Standardize column names, remove redundant indices, and handle missing values.
* **Feature Engineering:** Transform numeric agreement scores into categorical levels and map granular comment types (`-`, `HS`, `V`) into unified target classes (`Neutral`, `Hate`, `Vulgar`).
* **Statistical Insights:** Analyze text length distributions (word and character counts) across platforms and toxicity labels.
* **Visualization:** Generate clear, high-resolution plots illustrating class imbalances and feature correlations using Seaborn and Matplotlib.

---

## 🗂️ Dataset Structure

The dataset contains the following key columns:
* `Platform`: Source social media platform (`Twitter`, `Facebook`, `YouTube`).
* `Comment`: The raw Arabic text comment.
* `Type`: Granular classification (`-` for Neutral, `HS` for Hate Speech, `V` for Vulgar).
* `Agreement`: Annotator consensus scores.
* `Offensive_Level`: Binary or categorical severity labels (`Offensive` vs. `Non-Offensive`).

---

## 🛠️ Workflow & Methodology

1. **Loading & Inspection:** Initial data profiling to check shape, data types, and null values.
2. **Data Cleaning:** 
   * Stripping whitespace and normalizing Arabic text formatting.
   * Mapping raw code labels into intuitive category names.
3. **Feature Creation:** 
   * Extracting text length metrics (`word_count`, `char_count`).
   * Binning agreement scores into categorical levels (`total` vs. `partial`).
4. **Exploratory Data Analysis (EDA):**
   * Distribution plots of comment lengths.
   * Cross-tabulation of offensive language types by platform.
   * Class imbalance evaluation to guide downstream machine learning model training.

---

## 🚀 Getting Started

### Prerequisites
Make sure you have Python 3.8+ installed along with the required data science libraries:
```bash
pip install pandas numpy matplotlib seaborn
```

### Running the Analysis
Clone the repository and run the EDA script or Jupyter Notebook:
```bash
git clone https://github.com/your-username/arabic-offensive-language-eda.git
cd arabic-offensive-language-eda
jupyter notebook eda_pipeline.ipynb
```

---

## 📊 Sample Visualizations

* **Class Distribution:** Highlights the proportion of neutral vs. toxic comments.
* **Platform Breakdown:** Compares hate speech and vulgarity frequency across Twitter, Facebook, and YouTube.
* **Length Analysis:** Visualizes whether toxic comments tend to be shorter or longer than non-toxic ones.

---

## 🤝 Contributing
Contributions, suggestions, and feature requests are welcome! Feel free to open an issue or submit a pull request.

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).