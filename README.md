# DistilBERT-Text-Classification
Fine-tuning DistilBERT for text classification using a custom dataset

## Project Overview
This project demonstrates how to fine-tune the pre-trained DistilBERT model for text classification tasks. It involves training the model on a custom dataset, applying fine-tuning techniques, and evaluating its performance on test data.

## Features
Fine-tuned DistilBERT for binary text classification.
Enhanced performance using layer unfreezing and reduced learning rates.
Metrics for evaluation: accuracy, precision, recall, F1-score.
Visualizations of label distribution, training progress, and confusion matrix.

## Dataset
Training Data: Text samples labeled as positive or negative.
Validation Data: Used for hyperparameter tuning and monitoring performance during training.
Test Data: For evaluating the final model's performance.

Example text format:
label,text
0,This is a negative example.
1,This is a positive example.

## Model Architecture
Base Model: DistilBERT (distilbert-base-uncased from Hugging Face Transformers library).
Fine-tuning: Unfroze last layers for additional optimization on domain-specific data.

## Results
Initially, the model achieved 69.4% accuracy on the test set. After fine-tuning with val.csv at a lower learning rate, the test accuracy improved to 76.6%. Further fine-tuning by unfreezing additional layers pushed it up to 81.1%.
Fine-tuning significantly boosted performance.

## For Further Improvments :
Trying different learning rates, batch sizes and epochs could get better results.
I can try experimenting with unfreezing more layers that may enhance the model's ability to adapt.
Using additional data relevant to the target domain could improve the model’s generalization, especially if the validation or test set distribution differs from the training data.
