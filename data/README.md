# Data 

The data for this project is located here and the structure is as follows:

'''
- data/
  - Merged_Responses.csv
  - UGIB_generations_temp_0.8/
    BASE-GPT3.5.csv
    BASE-GPT4.csv
    ...
'''

The golden data and the generated data are stored in the `Merged_Responses.csv` file and the `UGIB_generations_temp_0.8` folder, respectively.

1. `Merged_Responses.csv` contains the questions and the golden answers from 5 experts named 'Laine', 'Gralneck', 'Sung', 'Gracia-Tsao', and 'Barkun'. Each line contains a question in text and its word count, the golden answers from the 5 experts with their word counts. There are totally 9 questions and 4 scenarios.

2. In `UGIB_generations_temp_0.8` folder, there are several '.csv' files, each of which is generated from a language model (e.g. GPT3.5) For each model, it acts as a student and generates answers for all the 9+4 questions and scenarios, each question with several answers. For each line (some answers have several lines), it contains the index of the question, followed by the answer in text.
