# Stress Analysis in Social Media 
Social media is one of the most common way for people to express "stress" nowadays. Therefore, I conducted a sentiment 
analysis to extract information and identify stress from social media posts. This project leverages the power of 
natural language processing (NLP) and supervised learning to build models that accurately classify stressful and 
non-stressful posts. It was inspired by the newly published paper called
[Dreaddit: A Reddit Dataset for Stress Analysis in Social Media](https://arxiv.org/abs/1911.00133).

For more information, please check out [Slides](https://bit.ly/37WNKbu)

## Requisites
- MacOS or Linux
- Python 3.7.4
- conda 
- pip
- GPU (To run BERT model)

## Setup
To setup the environment, please follow these steps:

- Clone the GitHub repository
```
git clone https://github.com/shahzadsaddique/NLP-and-Supervised-Learning-for-stress-analysis.git
```
- Navigate to project root and run the notebook
  ```
  /notebook/Stress_Analysis_Embedding.ipynb
  ```
  
- Our contribution

<img src="https://github.com/shahzadsaddique/NLP-and-Supervised-Learning-for-stress-analysis/blob/main/img/contribution-code.png" />


## Analysis
In this project, I trained the dataset with three feature extraction models TF-IDF, Word2Vec with TF-IDF as weights and 
BERT. After extracting the features, I trained the features with traditional classification models such as logistic
regression, SVM and random forest. Besides, BERT uses a fine tuning neural network to classify the text based on sentences. 

### New Model results
In this experiment, we trained the dataset with feature extraction models Word2Vec with TF-IDF as weights. After extracting the features, we first found the best hyperparameter settings and then trained the features with traditional classification models such as logistic regression, SVM, linear SVC and random forest etc. 

- In the original implementation the Precision for Word2Vec + TF-IDF was 69.4% with Random Forest classifier, but in our enhanced models, Linear SVC did a great job with Precision 71.71%


-  Recall is the most important metric because we want to identify the stress posts accurately. However, we also want to prevent misclassifying a lot of non-stress posts as stress post


- In the original implementation Recall was 84.8% which misclassified a lot of non-stress as stress, but in our enhanced models Recall was decreased to 78.31% which is a good sign for stress classification


- F1-Scores were bit decreased in our implementation then the original implementation

| Feature Extraction Model | Best Classification Model | Precision | Recall | F1-Score |
| :---------------- | :-------------  | :-------- |:-------| :------- |
| Word2Vec + TF-IDF | Linear SVC   | 71.71%     | 78.3%  | 74.3%    |

### Word2Vec (with TF-IDF) Prediction Results After improvement

<img src="https://github.com/shahzadsaddique/NLP-and-Supervised-Learning-for-stress-analysis/blob/main/img/results.png"  />


For more information, please check the notebook directory to see the analysis results of different models.


## Reference
- [Dreaddit: A Reddit Dataset for Stress Analysis in Social Media](https://arxiv.org/abs/1911.00133)

