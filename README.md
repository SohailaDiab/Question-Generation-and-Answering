# Question Generation and Answering
![image](https://user-images.githubusercontent.com/70928356/230603087-a6cac885-aea3-4289-8e98-ed101a2adc63.png)

## The Goal 
Automatically generate questions and answers, given any piece of text.

## Benefits
Using question generation and answering models can provide several benefits for businesses. Some of these benefits include:
- **Improved customer service:** By using question generation and answering models, businesses can quickly provide answers to customers' questions, reducing the need for human customer service representatives and improving response times.
- **Enhanced educational content**: These models can be used to create quizzes and assessments for educational content, allowing students to test their knowledge and gain a deeper understanding of the material.
- **Time-saving**: Generating questions and answers manually can be a time-consuming process, particularly for large volumes of text. Using automated models can save time and resources, allowing businesses to focus on other priorities.

## The Process
![image](https://user-images.githubusercontent.com/70928356/230604555-6f1b0e3d-1075-418a-a2e6-ea4ca814b7f5.png)

1. **Raw text is cleaned and preprocessed:**
    - Text is converted to lowercase
    - Arabic words are removed
    - Emails are removed 
    - Random numbers are removed
    - Citations, eg. [20] are removed
    - Expand contractions (I'm -> I am)
    - Hyphens, colons, semi-colons and full stops (-:;,) are removed
    - Slashes (\ / \ //) are removed
    - Extra spaces are removed
2. **Important key phrases are extracted from the preprocessed text**
    - Preprocessed text os passed to the key phrase extraction algorithms
    - Used key phrase extraction algorithms:
      - FirstPhrases 
      - KPMiner 
      - YAKE 
      - TextRank 
      - TopicRank 
      - Kea 
3. **Questions are generated**
    - Key phrases are passed on to the **T5 model** to generate questions
4. **Answers are generated**
    - T5 model's questions are passed on to **AllenNLP** and **HayStack**

## Notebooks
|                          Name                   |     Link     |
| ----------------------------------------------  |  ----------  |
| [Key Phrase Extraction and Question Generation](https://github.com/SohailaDiab/Question-Generation-and-Answering/blob/main/KeyExtract_QuesGen.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SohailaDiab/Question-Generation-and-Answering/blob/main/KeyExtract_QuesGen.ipynb) |
| [Question Answering using AllenNLP](https://github.com/SohailaDiab/Question-Generation-and-Answering/blob/main/Question_Answering_AllenNLP.ipynb)                         | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SohailaDiab/Question-Generation-and-Answering/blob/main/Question_Answering_AllenNLP.ipynb) |
| [Question Answering using HayStack](https://github.com/SohailaDiab/Question-Generation-and-Answering/blob/main/Question_Answering_HayStack.ipynb)                             | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SohailaDiab/Question-Generation-and-Answering/blob/main/Question_Answering_HayStack.ipynb) |
