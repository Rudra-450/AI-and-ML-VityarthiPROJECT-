# 📧 Spam Email Classifier — AIML Project

A machine learning project that classifies messages as **Spam** or **Ham (Not Spam)** using the **Naive Bayes algorithm** with text vectorization.

---

## 📁 Project Structure

```
spam-classifier/
│
├── spam.csv           # Dataset with labeled spam and ham messages
├── spam_classifier.py # Main Python script
└── README.md          # Project documentation
```

---

## 📊 Dataset (`spam.csv`)

The dataset contains **100 labeled messages** with two columns:

| Column  | Description                          |
|---------|--------------------------------------|
| `label` | `spam` or `ham` (not spam)           |
| `text`  | The actual email/message content     |

### Sample Data

| label | text                                                                 |
|-------|----------------------------------------------------------------------|
| ham   | Hey, are you coming to the meeting tomorrow at 10 AM?                |
| spam  | Congratulations! You have won a $1000 gift card. Click here!         |
| ham   | Can you please send me the project report by end of day?             |
| spam  | URGENT: Your bank account has been suspended. Verify your details.   |

---

## ⚙️ How It Works

```
Raw Text Messages
       ↓
CountVectorizer (Text → Numeric Matrix)
       ↓
Train/Test Split (80% train, 20% test)
       ↓
Multinomial Naive Bayes Model
       ↓
Predict: SPAM or HAM
```

### Step-by-Step Explanation

1. **Load Dataset** — Read `spam.csv` using Pandas.
2. **Feature Extraction** — `CountVectorizer` converts text into a bag-of-words matrix (word frequency counts).
3. **Train/Test Split** — 80% of data is used for training, 20% for evaluation.
4. **Model Training** — `MultinomialNB` learns patterns that distinguish spam from ham.
5. **Evaluation** — Accuracy score is computed on the test set.
6. **Prediction** — User can input a custom message to get a real-time prediction.

---

## 🚀 Getting Started

### Prerequisites

Make sure you have Python 3.x installed along with the following libraries:

```bash
pip install pandas scikit-learn
```

### Run the Project

```bash
python spam_classifier.py
```

You will see the model accuracy printed, then you can type any message to get a prediction:

```
Model Accuracy: 0.97
Enter a message: You have won a free iPhone! Click here to claim now.
Prediction: spam
```

---

## 🧠 Algorithm Used

### Multinomial Naive Bayes

- Best suited for **text classification** tasks with word frequency features.
- Based on **Bayes' Theorem**: calculates the probability that a message belongs to each class (spam/ham).
- Fast, lightweight, and performs well even with small datasets.
- Works great with `CountVectorizer` (bag-of-words representation).

---

## 📈 Model Performance

| Metric         | Description                                           |
|----------------|-------------------------------------------------------|
| **Accuracy**   | Percentage of correctly classified messages           |
| **Training**   | 80 messages used to learn spam/ham patterns           |
| **Testing**    | 20 messages used to evaluate model performance        |
| **Expected**   | ~95–98% accuracy on the provided dataset              |

---

## 🛠️ Technologies Used

| Tool / Library      | Purpose                              |
|---------------------|--------------------------------------|
| Python 3.x          | Programming language                 |
| Pandas              | Data loading and manipulation        |
| Scikit-learn        | ML model, vectorizer, and splitting  |
| CountVectorizer     | Text to numeric feature conversion   |
| MultinomialNB       | Naive Bayes classification algorithm |

---

## 💡 Future Improvements

- Use **TF-IDF Vectorizer** instead of CountVectorizer for better accuracy.
- Try other models like **Logistic Regression** or **SVM** for comparison.
- Add a **web interface** using Flask or Streamlit.
- Use a **larger real-world dataset** like the UCI SMS Spam Collection.
- Add **confusion matrix** and **classification report** for deeper evaluation.


---

## 👨‍💻 Submitted by:

-Rudra Kumar Pathak
-25MIM10177

---
