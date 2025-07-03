Sentiment Analysis using TF-IDF & Logistic Regression
- Company  : CODETECH IT SOLUTIONS PVT
- Name     : Dhupam Renuka Padmavathi 
- Intern Id :
- Domain    : Machine learning 
- Duration : 6 weeks 
- Mentor: Neela Santosh Kumar 

This repository contains a self-contained, beginner-friendly notebook that walks through building a classical Sentiment Analysis pipeline:

1. 🔄 Data loading & cleaning


2. ✨ Text preprocessing


3. 🏷 TF-IDF feature extraction


4. 🤖 Logistic-Regression model training


5. 📊 Evaluation & visualzation 

📂 Repository structure

.
├── Sentimental Analysis using TF-IDF.ipynb  # Main tutorial notebook
└── README.md                                # You are here

(If you convert the notebook to a plain .py script the same steps and function names apply.)


---

🛠️ Prerequisites

Package	Tested version	Install

Python	3.9+	—
pandas	2.2	pip install pandas
numpy	1.26	pip install numpy
scikit-learn	1.5	pip install scikit-learn
matplotlib	3.9	pip install matplotlib
seaborn	0.14	pip install seaborn


Create an isolated environment (recommended):

python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt  # optional helper file


---

🚀 Quick-start

1. Clone or download the repository.


2. Verify the dependencies above are installed.


3. Open the notebook:

jupyter notebook "Sentimental Analysis using TF-IDF.ipynb"


4. Run all cells (Kernel ▸ Restart & Run All).



The notebook will:

Fetch the sample Twitter dataset (≈1.6 M rows) from GitHub.
You can comment out the download line and point url to a local file instead.

Clean the text (lower-casing, punctuation removal, stop-word filtering, lemmatisation).

Convert text to a sparse TF-IDF matrix (max_features=5000 by default).

Split the data into 80 % train / 20 % test with a fixed random_state for reproducibility.

Fit a Logistic Regression classifier with L2 regularisation.

Evaluate accuracy, precision, recall & F1 and plot a confusion-matrix heat-map.



---

🔄 Customising for your own data

What to change	Where	Typical tweak

Data source	url = ...	Replace with local CSV path or pd.read_json(...)
Text column name	df['review']	Rename to your column
Label column name	df['sentiment']	Rename (positive, negative, neutral, etc.)
Language / preprocessing	preprocess_text()	Add language-specific rules, e.g. stemming
Vectoriser size	TfidfVectorizer(max_features=5000)	Increase for larger vocab
Algorithm	LogisticRegression()	Swap for SVM, XGBoost or neural nets



---

📈 Expected results

With the default settings you should observe ≈83-85 % accuracy on the sample Twitter data.
Exact numbers will vary according to sklearn versions and random splits.

A correctly sized confusion matrix appears similar to:

Predicted
           Negative  Positive
Actual
Negative      5 890      1 210
Positive      1 050      5 930


---

📝 Experiment tracking

For serious experimentation, consider:

Adding MLflow for parameter tracking.

Saving the fitted model with joblib.

Performing cross-validation (GridSearchCV) to tune C and max_features.



---

⚠️ Troubleshooting

Symptom	Fix

MemoryError during TF-IDF	Lower max_features or batch-process data
Poor accuracy	Check class-balance, try stratified split
UnicodeDecodeError on load	Ensure correct file encoding, e.g. encoding='utf-8-sig'



---

🤝 Contributing

Pull requests are welcome! Please open an issue first to discuss significant changes.

1. Fork the repo and create your branch: git checkout -b feature/foo


2. Commit your changes: git commit -m 'Add some foo'


3. Push to the branch: git push origin feature/foo


4. Open a Pull Request


📜 License

This project is released under the MIT License. See LICENSE for details.


🙏 Acknowledgements

Twitter Sentiment dataset courtesy of the Kaggle community.

