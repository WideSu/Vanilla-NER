# Multi-language Named Entity Recognition

# Task Description
Named entity recognition (NER) is the task of tagging entities in text with their corresponding type. Approaches typically use BIO notation, which differentiates the beginning (B) and the inside (I) of entities. O is used for non-entity tokens.

# Content
This repo includes the code for training a flair model using stacked embeddings (with word and flair contextual embeddings) to perform named entity recognition (NER). The dataset used is the CoNLL 2003 dataset for NER (train, dev) with a manually corrected (improved/cleaned) test set from the CrossWeigh paper called CoNLL++. The current state-of-the-art model on this dataset is from the CrossWeigh paper (also using flair) by Wang et al. (2019) with F1-score of 94.3%. Without using pooled-embeddings, CrossWeigh and training to a max 50 instead of 150 epochs, we get a micro F1-score of 93.5%, within 0.7 of a percentage point of the SOTA.

The notebook is structured as follows:

- Setting up the GPU Environment
- Getting Data
- Training and Testing the Model
- Using the Model (Running Inference)

# Data 
- Chinese corpos: flair.datasets.NER_CHINESE_WEIBO()
- English corpos: CoNLL++
