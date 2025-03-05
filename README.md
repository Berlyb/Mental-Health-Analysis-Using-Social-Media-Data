# Mental Health Analysis Using Social Media Data

## Project Overview
This project leverages **Natural Language Processing (NLP)** and **Machine Learning (ML)** techniques to analyze mental health patterns in social media posts. By focusing on the **McGill University subreddit**, the goal is to detect signs of **depression** and **stress** among students. This analysis aims to assist **university administrators** and **mental health professionals** in identifying key areas of concern and promoting timely interventions during stressful academic periods.

## Objectives
- Detect and classify mental health challenges (depression and stress) from social media posts.
- Analyze the **frequency** and **timing** of these challenges throughout the academic year.
- Use **topic modeling** to extract themes from stress- and depression-related discussions.

## 📊 Methodology
### 1. Data Collection
- **Training Data:**
  - Depression Dataset (Kaggle) - **7,732 rows**
  - Stress Detection Dataset (Social Media) - **5,557 rows**
- **Testing Data:**
  - **McGill University Subreddit** - Scraped **2,800 posts** using **BeautifulSoup**.

### 2. Text Preprocessing
The data underwent rigorous cleaning using the following steps:
- **Tokenization:** Splitting text into words
- **Stopword Removal:** Removing common, uninformative words
- **Lemmatization:** Reducing words to their base form
- Removing **non-alphabetic characters**, **URLs**, **symbols**, and **emojis**

Final dataset: **2,592 clean, unique subreddit posts**

### 3. Model Development
We applied two text vectorization techniques and four ML classifiers:

#### Text Vectorization Methods:
- **Word2Vec:** Word embedding to capture contextual meaning
- **TF-IDF:** Term Frequency-Inverse Document Frequency for keyword importance

#### Machine Learning Models:
- **Logistic Regression**
- **Support Vector Machines (SVM)**
- **Random Forest**
- **AdaBoost**

**Feature Engineering:**
- Vocabulary limited to the **top 3,000** words
- Ignored words appearing in **less than 2** or **more than 95%** of documents
- Applied **StratifiedKFold** cross-validation (5 folds) for model evaluation



## 🧰 Tools and Libraries
- **Python** (for model development and analysis)
- **pandas**, **numpy**, **scikit-learn** (data processing and modeling)
- **NLTK**, **VADER** (NLP and sentiment analysis)
- **BeautifulSoup** (web scraping)
- **LDA** (Latent Dirichlet Allocation for topic modeling)

## 📌 How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/mental-health-analysis.git
   cd mental-health-analysis
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure the dataset files are in the `/data` directory.

4. Run the main analysis script:
   ```bash
   python main.py
   ```



### Future Improvements
- Explore advanced **deep learning models** (e.g., BERT for contextual understanding).
- Expand the dataset to **other university subreddits** for comparative analysis.
- Implement **real-time monitoring** of mental health signals.


---
This project demonstrates the power of **social media analysis** for **early detection** of student mental health challenges and offers a foundation for designing **targeted mental health interventions**.

