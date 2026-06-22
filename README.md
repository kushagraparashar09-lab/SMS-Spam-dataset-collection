import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.linear_model import LogisticRegression
from sklearn.pipeline import Pipeline

# dataset auto download (NO ERROR)
url = "https://raw.githubusercontent.com/justmarkham/pycon-2016-tutorial/master/data/sms.tsv"
df = pd.read_csv(url, sep="\t", header=None)

df.columns = ['label', 'message']
df['label'] = df['label'].map({'ham':0,'spam':1})

print("Rows:", len(df))

X = df['message']
y = df['label']

X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.2,
    random_state=42,
    stratify=y
)

model = Pipeline([
    ('tfidf', TfidfVectorizer(stop_words='english', ngram_range=(1,2))),
    ('clf', LogisticRegression(max_iter=1000))
])

model.fit(X_train, y_train)

print("Accuracy:", model.score(X_test, y_test))

print(model.predict([
    "Free prize win money now",
    "Hey how are you"
]))
