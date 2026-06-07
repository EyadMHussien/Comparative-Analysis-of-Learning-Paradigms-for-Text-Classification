Comparative Analysis of Learning Paradigms for Text Classification
Overview
This project presents an advanced machine learning analysis comparing three distinct learning paradigms for text classification. It evaluates their performance, efficiency, and resource requirements using a specialized emotion classification task.

Dataset
Source: The project uses the dair-ai/emotion dataset from Hugging Face.

Task: Text is classified into exactly one of six emotion categories: sadness, joy, love, anger, fear, and surprise.

Distribution: The dataset is split into 16,000 training examples, 2,000 validation examples, and 2,000 test examples.

Models Compared
The notebook implements and compares the following architectures:

RNN (From Scratch): A custom-built Bidirectional LSTM and GRU.

Transformer (Fine-Tuned): A pre-trained bert-base-uncased model that is fine-tuned on the dataset.

Large Language Models (LLMs): Zero-shot, few-shot (3-shot and 8-shot), and Chain-of-Thought (CoT) prompting utilizing models like Phi-3 and Llama-3.2.

Key Results & Metrics
The models were evaluated based on Test Accuracy, Macro F1, Training Time, Inference Time, and Data Efficiency.

RNN — GRU (From Scratch): Achieved a test accuracy of 92.00% and a Macro F1 score of 0.8835. It had a fast training time of 70.9s and an inference time of 0.2628s.

Transformer — BERT (Fine-Tuned): Reached the highest test accuracy of 92.65% and a Macro F1 score of 0.8851. It required significantly more compute, with a training time of 512.9s and an inference time of 6.7480s.

LLM — Phi-3 CoT: Reached an accuracy of 53.05% and a Macro F1 score of 0.4302 exclusively through prompting, with an inference time of 7432.17s.

Data Efficiency
The project also explores the impact of limited training data by training the models on only 500 examples versus the full training set:

RNN: Accuracy heavily declined to 25.00% when restricted to 500 examples.

BERT: Accuracy heavily declined to 23.30% when restricted to 500 examples.

LLMs: Exhibited a baseline advantage in data efficiency because they require zero fine-tuning to perform the classification task.

Technologies Used
Libraries: PyTorch, Hugging Face transformers, and datasets for model building and evaluation.

Data Processing & Visualization: Pandas, Matplotlib, and Seaborn.
