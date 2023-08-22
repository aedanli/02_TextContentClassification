# 2_TextContentClassification
Build a content-based classifier to predict the category of text from an imbalanced unlabelled dataset.

## Motivation:
For a presentation on this project, see https://aedanyue.files.wordpress.com/2023/08/textclassification-2.pdf

A common goal is to determine whether text belongs to certain categories without knowledge of the class labels in advance, such as 1) identifying types of news article from the headline, 2) whether text is spam, 3) the text sentiment, or 4) identifying text from a bot.
In this project, let’s predict the category of news headline from an unlabelled dataset.

For the training set, we will use 210,000+ headlines scraped from Huffington Post between 2021-2022: https://www.kaggle.com/datasets/rmisra/news-category-dataset

For the unlabelled test set, we will use 20,000+ recent headlines scraped from BBC news, without class labels: https://www.kaggle.com/datasets/gpreda/bbc-news

## Summary:
- I preprocessed the text data with NLP and converted headlines to a TF-IDF matrix
- Visualized the TF-IDF matrix using dimensionality reduction algorithms & Topic Modelling using LDA
- Tuned classifier parameters using an imbalanced training set (1:10 ratio), reaching accuracy = 93% and AUC = 93%
- Found that class weights had the greatest impact on performance during tuning, revealing the importance of adequate training data samples
- Successfully generalized the classifier to predict whether BBC headlines were "Science" or "Not Science"

## Future Directions:
- Train on extremely imbalanced dataset (1:100 ratio)
- Try multiclass classification
- Try neural networks
- Generalize classifier to social media platforms (e.g., Reddit, Twitter)
