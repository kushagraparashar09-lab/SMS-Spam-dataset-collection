# 📩 SMS Spam Detection

A Machine Learning project that classifies SMS messages as **Spam** or **Ham (Not Spam)** using Natural Language Processing (NLP).

## 🚀 Features

- SMS text preprocessing
- Text cleaning and tokenization
- TF-IDF Vectorization
- Multiple Machine Learning models
- Spam prediction for custom messages
- Model evaluation with accuracy, precision, recall, and F1-score

## 📂 Dataset

This project uses the **SMS Spam Collection Dataset**, containing over 5,500 labeled SMS messages.

Dataset format:

| Label | Message |
|-------|---------|
| ham | Hey, are we meeting today? |
| spam | Congratulations! You've won a free prize. |

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Matplotlib
- Seaborn
- Jupyter Notebook

## 📁 Project Structure

```
SMS-Spam-Detection/
│
├── data/
│   └── spam.csv
│
├── notebooks/
│   └── sms_spam_detection.ipynb
│
├── models/
│   └── spam_model.pkl
│
├── app.py
├── requirements.txt
├── README.md
└── LICENSE
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/SMS-Spam-Detection.git
```

Move into the project folder:

```bash
cd SMS-Spam-Detection
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## ▶️ Usage

Run the application:

```bash
python app.py
```

Example:

```
Input:
Congratulations! You've won a FREE iPhone.

Output:
Spam
```

## 📊 Machine Learning Pipeline

1. Load dataset
2. Data preprocessing
3. Text cleaning
4. Tokenization
5. TF-IDF Vectorization
6. Train/Test split
7. Model training
8. Evaluation
9. Prediction

## 📈 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

## 📸 Sample Output

```
Message:
Hey, where are you?

Prediction:
Ham ✅
```

```
Message:
WIN a FREE vacation now!

Prediction:
Spam 🚨
```

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to your branch
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## ⭐ Support

If you found this project useful, please give it a ⭐ on GitHub!
