# Enhanced Detection of Domain Generation Algorithms (DGA) using Deep Learning Techniques

This repository contains code for training and evaluating models to classify domain names, focusing on the detection of Domain Generation Algorithms (DGA). The primary task is multi-class classification, where the model identifies subclasses such as dga, legit, gameoverdga, cryptolocker, newgoz, nivdort, goz, necurs, and bamital. Additionally, the model's performance is evaluated on a broader binary classification task of distinguishing between DGA and legitimate domains.

# Introduction 
Domain Generation Algorithms (DGA) are often used by malware to dynamically generate domain names for command-and-control servers, making detection challenging. Traditional detection methods rely on manually crafted features, but in this project, we explore deep learning techniques to enhance detection accuracy. By leveraging advanced models, we aim to improve detection performance over conventional approaches.

# Dataset 
The dataset used is sourced from [Kaggle: DGA Dataset](https://www.kaggle.com/datasets/gtkcyber/dga-dataset). It was compiled from the Alexa website ranking and includes a blacklist of past DGA domain names. The dataset consists of four columns:

- isDGA: Binary labels ('dga' or 'legit')
- domain: The domain name itself
- host: The domain with Top-Level Domain (TLD)
- subclass: Contains 9 unique classes (gameoverdga, cryptolocker, newgoz, nivdort, goz, necurs, bamital, alexa, and legit)

# Models
The project utilizes multiple models to approach the classification tasks:

- Baseline: Random Forest
- Neural Network: Convolutional Neural Network (CNN) & Recurrent Neural Network (RNN)
- Transformer Models: Original Transformer Encoder & Pre-trained BERT

# Results 
- CNN: Achieved a macro accuracy of 84%, showing strong capability in identifying local patterns within domain names. Some misclassifications were noted, indicating room for further tuning.
- RNN with CNN: Combining sequential and pattern recognition, this model attained the highest ROC-AUC score of 97%, effectively ranking the correct class with high confidence.
- Transformers: Achieved the highest True Negative Rate (TNR) of 99.9% for the binary classification task, although it showed lower performance on the multi-class classification. This suggests a need for further tuning to handle multi-class complexity effectively within limited resources.

# Reprt 
For a detailed report, see this [document](https://docs.google.com/document/d/1KMnWt9wKVOk078Qmj2BtH0CNdobcQplY/edit?usp=sharing&ouid=110791519566382968918&rtpof=true&sd=true).
