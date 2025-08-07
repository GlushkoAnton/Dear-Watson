Contradictory, My Dear Watson

This project is part of the Kaggle competition, which focuses on natural language inference (NLI) — the task of determining the logical relationship between pairs of sentences. The objective is to classify whether the second sentence (hypothesis) contradicts, entails, or is neutral with respect to the first (premise).

Problem Description

Given a pair of sentences:
	•	Premise
	•	Hypothesis

The model must predict one of three classes:
	•	Entailment
	•	Neutral
	•	Contradiction

This is a multilingual dataset, including multiple languages. The challenge is both semantic and linguistic.

Approach

The baseline approach involves:
	•	Text preprocessing
	•	Tokenization using pretrained multilingual transformers (e.g. XLM-Roberta)
	•	Fine-tuning a transformer model on the provided dataset
	•	Evaluation using accuracy metric

You can modify or improve the pipeline using:
	•	Language-specific preprocessing
	•	Data augmentation
	•	Advanced transformer heads
	•	Ensembling or cross-lingual techniques

Dataset
	•	train.csv: labeled sentence pairs with language information
	•	test.csv: unlabeled pairs for prediction
	•	sample_submission.csv: required format for submission

How to Run
	1.	Install dependencies:

pip install -r requirements.txt


	2.	Train the model:

python train.py


	3.	Generate predictions:

python predict.py


Evaluation Metric
	•	The model is evaluated based on classification accuracy on unseen sentence pairs.

References
	•	Multilingual Natural Language Inference (XNLI)
	•	Hugging Face Transformers
	•	XLM-Roberta paper

