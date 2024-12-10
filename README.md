# Mathception-Unraveling-Misconceptions
Predict affinity between misconceptions and incorrect answers (distractors) in multiple-choice questions

Eedi - Mining Misconceptions in Mathematics

- Overview

In this competition, you’ll develop a Natural Language Processing (NLP) model driven by Machine Learning (ML) to accurately predict the affinity between misconceptions and incorrect answers (distractors) in multiple-choice questions. This solution will suggest candidate misconceptions for distractors, making it easier for expert human teachers to tag distractors with misconceptions.

Goal: Predict the relationship between misconceptions and distractors, helping human labelers tag distractors with misconceptions more efficiently and consistently.

- Background

A Diagnostic Question (DQ) is a multiple-choice question with four options: one correct answer and three distractors (incorrect answers). Each distractor is crafted to represent a specific misconception.

For example, if a student selects the distractor "13," they may have the misconception, "Carries out operations from left to right regardless of priority order."

Tagging distractors with misconceptions is crucial but time-consuming. It is also difficult to maintain consistency across multiple human labelers. Misconceptions vary in terms of description granularity, and new misconceptions emerge over time.

Initial efforts using pre-trained language models have not been successful, likely due to the complexity of the mathematical content. Therefore, a more efficient approach is needed to streamline the tagging process and enhance the quality of the results.

- Dataset

The data consists of Diagnostic Questions where each question has one correct answer and three distractors. Each distractor corresponds to a specific misconception. The dataset includes:

train.csv: Training data for model development, with labeled misconceptions. https://1drv.ms/u/s!AmlaN4R9CsYBhrZr2gR_W_HPdguI5A?e=9jXOO6

test.csv: Test data for model evaluation. https://1drv.ms/u/s!AmlaN4R9CsYBhrZp1C1KbTn2YztydA?e=6kyNz1

misconception_mapping.csv: Maps MisconceptionId to its MisconceptionName. https://1drv.ms/u/s!AmlaN4R9CsYBhrZn1_IfaP9tPWlRbg?e=YtmPy4

sample_submission.csv: Example submission format. https://1drv.ms/u/s!AmlaN4R9CsYBhrZo5MQPieSMeeMUNw?e=HR1GVb


- File Details
train.csv
QuestionId: Unique question identifier
ConstructId: Unique construct identifier
ConstructName: Granular knowledge related to question
CorrectAnswer: A/B/C/D (char)
SubjectId: Unique subject identifier
SubjectName: Broader context than the construct
QuestionText: Question text extracted using OCR
Answer[A/B/C/D]Text: Option A/B/C/D text
Misconception[A/B/C/D]Id: Ground truth labels
misconception_mapping.csv

MisconceptionId: Unique misconception identifier
MisconceptionName: Description of the misconception
sample_submission.csv

QuestionId_Answer: Each question has three incorrect answers. Predict MisconceptionIds.

- Acknowledgments

Eedi, Vanderbilt University, and The Learning Agency Lab would like to thank the Bill & Melinda Gates Foundation, Schmidt Futures, and the Chan Zuckerberg Initiative for their support in making this work possible.

- Files

train.csv (Size: 911.34 KB)

test.csv

misconception_mapping.csv (Size: 197.81 KB)

sample_submission.csv

- Data License

This data is licensed under the Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).

- Problem Description

You are tasked with predicting the MisconceptionIds for three incorrect answers for each question in the test set. The MisconceptionId is space delimited for each set of predictions.

Files for Submission
train.csv
Contains labeled data for training the model.

test.csv
Contains test data on which to evaluate the model.

misconception_mapping.csv
Provides the mapping of MisconceptionIds to their names.

sample_submission.csv
Example format for the submission file.

- Evaluation

Accuracy and F1-score will be used as evaluation metrics.
Models should aim to improve accuracy in predicting misconceptions for distractors.

- Conclusion

This project seeks to predict the correct misconceptions from the distractors in multiple-choice questions. The task leverages NLP techniques, ML models, and feature engineering to achieve accurate predictions and streamline the tagging process for human labelers.
