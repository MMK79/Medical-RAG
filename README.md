# Question Answering on MEDMCQA Dataset

This repository provides a streamlined approach to answer multiple-choice medical questions using the MEDMCQA dataset. We employ a simple Retrieval-Augmented Generation (RAG) method.

* Check the Comments of the Code
* Check the Medical RAG Project Tips to understand the challenges \& tips that you might face when you want to do it yourself

## Notebooks Overview

1. **`01-mlm_finetune_bert.ipynb`**:
    - Fine-tunes the BioClinical BERT model on the MEDMCQA dataset. (25 epochs, 40k dataset, Kaggle run (2 T4 GPU)) --> around 4 hour run
        * You can use Kaggle jupyter server to write your Code in VS Code and use Kaggle resource to run it
        * You can write the code in Kaggle and use save version feature so you don't need to stay in kaggle to see the run
    - Pushes the resulting model to Hugging Face repository.

2. **`02-preprocess_medmcqa.ipynb`**:
    - Creates the database which is going to be used for retrieving similar questions. The CLS (Classification) embeddings of the questions are added to this database to use them for finding the most relevant questions to the user's query.
    - Pushes the processed dataset to your Hugging Face repository.