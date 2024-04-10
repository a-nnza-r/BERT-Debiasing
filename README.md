# BERT Debiasing Project

## Purpose

The purpose of this project is to address and mitigate gender bias in the embeddings generated by the BERT (Bidirectional Encoder Representations from Transformers) model. By modifying the BERT model to process inputs in batches and apply Principal Component Analysis (PCA), we aim to identify and remove components that contribute to gender bias, resulting in more equitable and unbiased representations.

## Methodology

The methodology of this project involves several key steps:

1. **Modification of BERT Model**: We start by defining a custom BERT model class that allows for layer-wise embedding adjustment, specifically targeting the principal components that capture gender bias.
2. **Data Preparation**: We generate sentence pairs that differ only in gender-specific pronouns and associated occupations, ensuring a wide coverage of gender representation in different professional contexts.
3. **Debiasing Process**: The custom BERT model processes these sentence pairs to compute debiased embeddings and identify the principal components of gender bias at each layer.
4. **Evaluation**: To assess the effectiveness of the debiasing process, we compare the gender predictability of the original and debiased embeddings using a logistic regression model. A decrease in the model's accuracy in predicting gender after debiasing indicates a successful reduction of bias.

## Outcomes and Conclusions

The project's primary outcome is the successful development and implementation of a debiasing process that reduces gender bias in BERT embeddings. Our experiments show that the logistic regression model's ability to predict gender based on embeddings significantly decreases after applying our debiasing method, indicating effective bias mitigation.

In conclusion, this project demonstrates the feasibility of debiasing BERT embeddings to reduce gender bias. Future work can extend this approach to other forms of bias and explore further enhancements to debiasing techniques. The principal components analyzed in this study offer valuable insights into the nature of gender representation in BERT embeddings and provide a foundation for continued research in the field of ethical AI.
