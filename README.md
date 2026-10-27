Emotion Analysis Using NLP

Overview

This project focuses on emotion classification using Natural Language Processing (NLP) and machine learning. It analyzes text data and predicts the emotion expressed in a given text.

The project explores text preprocessing, feature extraction techniques, and multiple machine learning algorithms to compare their classification performance.

Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- Scikit-learn

Dataset

The project uses the Emotions Dataset for NLP, which contains text samples labeled with their corresponding emotions.

The dataset includes three files:

- "train.txt" — Training data
- "test.txt" — Testing data
- "val.txt" — Validation data

The dataset contains six emotion categories:

- Sadness
- Anger
- Love
- Surprise
- Fear
- Joy

Project Workflow

1. Data Loading and Exploration

- Load the dataset into Pandas DataFrames.
- Examine the dataset structure and emotion labels.
- Check for missing values.

2. Text Preprocessing

- Convert text to lowercase.
- Remove punctuation.
- Remove numbers and emojis.
- Remove English stopwords using NLTK.

3. Label Encoding

Convert emotion labels into numerical values so they can be used by machine learning algorithms.

4. Feature Extraction

Bag of Words (BoW)

Uses word-frequency-based features to represent text numerically.

TF-IDF (Term Frequency–Inverse Document Frequency)

Represents text using word importance scores, helping distinguish informative words from common terms.

5. Model Training

Three machine learning approaches are explored:

- Multinomial Naive Bayes with Bag of Words
- Multinomial Naive Bayes with TF-IDF
- Logistic Regression with TF-IDF

6. Model Evaluation

The models are evaluated using accuracy on the test data.

Results

Model| Feature Extraction| Accuracy
Multinomial Naive Bayes| Bag of Words| 76.81%
Multinomial Naive Bayes| TF-IDF| 66.09%
Logistic Regression| TF-IDF| 86.28%

Logistic Regression with TF-IDF achieved the highest accuracy among the three approaches tested in this notebook.

Repository Structure

NLP/
└── NLP/
    ├── emotionanalysis.ipynb
    ├── README.md
    └── dataset/
        ├── train.txt
        ├── test.txt
        └── val.txt

How to Run

1. Clone the repository:
   
   git clone YOUR_GITHUB_REPOSITORY_URL

2. Navigate to the project directory:
   
   cd NLP

3. Install the required libraries:
   
   pip install pandas numpy matplotlib seaborn scikit-learn nltk

4. Download the NLTK resources required by the notebook:
   
   import nltk

nltk.download('punkt')
nltk.download('stopwords')

5. Open "emotionanalysis.ipynb" in Jupyter Notebook or Google Colab.

6. Update the dataset file paths to match your local directory and run the notebook cells in order.

Key Learnings

- Text preprocessing and cleaning
- Stopword removal using NLTK
- Converting categorical labels into numerical values
- Bag of Words and TF-IDF vectorization
- Training and evaluating text classification models
- Comparing machine learning algorithms using accuracy

Future Improvements

- Evaluate models using precision, recall, F1-score, and a confusion matrix.
- Tune model hyperparameters to improve performance.
- Experiment with additional classification algorithms.
- Explore deep learning and transformer-based NLP models.

Dataset Attribution

The dataset used in this project is the Emotions Dataset for NLP available on Kaggle. Please refer to the original dataset page for its licensing and attribution requirements.
