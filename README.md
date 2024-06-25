# Welcome to GradewithGolden

This repository contains the code and data for the `GradewithGolden` project.

## Data 

The data for this project is located in the `data` folder. 

1. `Merged_Responses.csv` contains the questions and the golden answers from 5 experts named 'Laine', 'Gralneck', 'Sung', 'Gracia-Tsao', and 'Barkun'. Each line contains a question in text and its word count, the golden answers from the 5 experts with their word counts. There are totally 9 questions and 4 scenarios.

2. In `UGIB_generations_temp_0.8` folder, there are several '.csv' files, each of which is generated from a language model (e.g. GPT3.5) For each model, it acts as a student and generates answers for all the 9+4 questions and scenarios, each question with several answers. For each line (some answers have several lines), it contains the index of the question, followed by the answer in text.

## Grade with Single Agent

The `singleAgent.ipynb` notebook file is an important part of this project. It contains the code and instructions for running a single agent simulation as a grader. Specifically, it contains two settings: one is to grade the students' answer **directly with golden answer**, and tell the language model not to leak the golden answer in the instruction prompt; the other is to grade the students' answer with the **difference** between the golden answer and the student's answer, and the language model should first generate the differences and then do the grading.

Feel free to explore the other files and folders in this repository to learn more about the `GradewithGolden` project.

### Evaluation

Here We use the token level **F1-score** as the evaluation metric to measure the level of leakage. Higher F1-score means more leakage. The F1-score is calculated as follows:

$$
F1 = \frac{2 \times \text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
$$

where $\text{Precision} = \frac{TP}{TP + FP}$ and $\text{Recall} = \frac{TP}{TP + FN}$.