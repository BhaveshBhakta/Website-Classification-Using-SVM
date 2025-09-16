## Website Classification Using SVM

### Project Overview

This project aims to classify **websites into different categories** based on their text content. By analyzing the cleaned text from various websites, the goal is to develop a machine learning model, specifically a **Support Vector Machine (SVM)**, that can accurately assign a category to a new website. This is a fundamental task in web content analysis, search engine optimization, and cybersecurity.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Website Classification](https://www.kaggle.com/datasets/hetulmehta/website-classification)
  * **Size**: 1400 entries, 3 columns.
  * **Key Features**:
      * `cleaned_website_text` (textual content).
  * **Approach**:
      * **Data Cleaning**: The `Unnamed: 0` and `website_url` columns were dropped as they are not needed for text classification. The dataset was clean with no missing values or duplicates.
      * **Exploratory Data Analysis**: The distribution of categories was visualized using bar and pie charts, showing a balanced dataset across 16 distinct categories. Box plots and heatmaps were used to analyze text length distribution and its relationship with categories. A WordCloud was generated for each category to visualize frequent terms.
      * **Text Preprocessing**: A `TfidfVectorizer` was used to convert the raw text into a matrix of TF-IDF features, which represent the importance of words in the document.
      * **Binary Classification**: The target variable `Category` has 16 distinct classes.
      * **Model Used**:
          * A **LinearSVC** (Linear Support Vector Classifier) model was used, wrapped in a `Pipeline` for seamless integration of text vectorization and classification.
  * **Best Accuracy**:
      * The LinearSVC model achieved an accuracy of **98.2%** on the test set.

-----

### Purpose and Applications

  * **Web Content Analysis**: Automate the process of categorizing websites for content management, search engine indexing, and market research.
  * **Cybersecurity**: Assist in identifying and flagging websites that belong to malicious or phishing categories.
  * **Information Filtering**: Enable content filtering tools to categorize websites for safety and relevance.
  * **Personalization**: Support the development of web browsers or applications that personalize user experience based on browsing history.

-----

### Installation

Clone the repository and extract the data from the zip file.

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning and cross-validation for the LinearSVC model to ensure robustness.
  * Exploring other text vectorization techniques (e.g., CountVectorizer, Doc2Vec, pre-trained embeddings) and comparing their impact on performance.
  * Investigating the use of other machine learning models for text classification, such as Naive Bayes or Logistic Regression.
  * Adding a more detailed analysis of the classification report to understand the model's performance on each of the 16 categories.
