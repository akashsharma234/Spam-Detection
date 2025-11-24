📌 Spam Classification using TF-IDF + Random Forest

This project builds a Spam Detector using machine-learning techniques.
It classifies SMS messages as Spam or Ham (Not Spam) using:

Text Cleaning

Stopword Removal

TF-IDF Vectorization

RandomForest Classifier

🚀 Project Workflow
1. Load Dataset

Read spam.csv

Remove unnecessary columns

Rename columns to:

label (spam/ham)

text (message content)

2. Clean the Text

Performed using the clean_text() function:

Convert to lowercase

Remove punctuation

Tokenize

Remove stopwords

Return cleaned tokens

3. Convert Text to Vectors (TF-IDF)

Used TfidfVectorizer with custom analyzer (clean_text) to convert text into numerical features.

4. Train/Test Split

Split the dataset into:

80% training

20% testing

5. Train the RandomForest Model

Fit using the TF-IDF features

Predict labels on test data

6. Evaluation Metrics

Calculated:

Precision

Recall

Example:

Precision: 1.00  
Recall: 0.87

7. Manual Testing

You can manually test your own SMS messages using:

text_tfidf = tfidf_vect.transform([message])
rf_model.predict(text_tfidf)

📦 Technologies Used

Python

Pandas

Scikit-Learn

NLTK

TF-IDF Vectorizer

RandomForestClassifier

Jupyter Notebook

🧪 Example Prediction
predict_message("Free entry in 2 a wkly comp to win FA Cup final tkts 21st May 2005")
# Output: 'spam'

📂 Project Structure
📁 spam-classifier/
├── spam.csv
├── notebook.ipynb
├── README.md
└── requirements.txt

🙌 Future Improvements

Try other models (Logistic Regression, SVM, Naive Bayes)

Use stemming or lemmatization

Try Word2Vec or BERT embeddings

Build a small UI for live predictions
