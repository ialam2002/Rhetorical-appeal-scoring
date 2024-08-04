# Rhetorical-appeal-scoring

This project focuses on training a RoBERTa model using PyTorch to score arguments on three rhetorical appeals: logos, pathos, and ethos. The dataset used for this project is `reddit_appeal_scores.csv`, and the code is implemented in a Python notebook: `rhetorical_appeal_scoring.ipynb`.

## Overview
The objective of this project is to develop a model capable of evaluating the rhetorical strength of arguments by scoring them on logos (logic), pathos (emotion), and ethos (credibility). This can be useful in analyzing speeches, articles, and other forms of persuasive communication.

## Dataset
The dataset used in this project is reddit_appeal_scores.csv, which contains 6000 Reddit comments labeled with scores for logos, pathos, and ethos.

- reddit_appeal_scores.csv: This file includes the columns argument_text, logos_score, pathos_score, and ethos_score.

This dataset are arguments collected using a reddit scraper from the subreddet `r/changemyview`. The arguments were then passed through `GPT-4` using another code to score the arguments to use for training.

## Model Architecture
We utilize the RoBERTa model, a robustly optimized BERT pretraining approach, as the base for our scorer. RoBERTa's effectiveness in various NLP tasks makes it an excellent choice for this project.

## Training
The model was trained using PyTorch. 

We fine-tuned the pre-trained RoBERTa model on our dataset to adapt it to the specific task of scoring rhetorical appeals.

## Evaluation
The performance of the model was evaluated using metrics such as Mean Squared Error (MSE) and R-squared (R²) for each of the three scores: logos, pathos, and ethos.
