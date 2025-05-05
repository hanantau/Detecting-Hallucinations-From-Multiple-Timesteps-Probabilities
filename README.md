Detecting Hallucinations From Multiple-Timesteps Probabilities
This project explores whether it's possible to detect hallucinations in generated answers by analyzing token-level probabilities across multiple timestamps.

📁 Repository Structure
qa-right.jsonl
A dataset of question-answer (QA) pairs where the answers are correct. Each record contains:

The question and correct answer

Top-10 predicted probabilities for every token in the answer

qa-hal.jsonl
A dataset of QA pairs where the answers include hallucinations. Each record includes:

The question and hallucinated answer

Top-10 predicted probabilities for each token

The index at which the hallucination starts

CLASSIFIERS.ipynb
A Jupyter Notebook containing:

Classifier implementations (e.g., logistic regression, SVM)

Evaluation of models that predict whether an answer contains a hallucination

🔍 Project Goal
We aim to detect hallucinated answers using only the token-level probability distributions produced during generation. This involves:

Treating the hallucination detection task as a time-series classification problem

Using datasets with annotated hallucination positions

Training and evaluating classifiers to predict the presence of hallucination based on token-level statistics

📊 Methodology
Extract statistical or temporal features from the per-token top-k probability distributions

Train classifiers to distinguish between correct and hallucinated answers

Evaluate performance on held-out test data

📌 Usage
Open the CLASSIFIERS.ipynb notebook and run the cells sequentially. It includes code for loading the datasets, feature engineering, training, and evaluating classifiers.
