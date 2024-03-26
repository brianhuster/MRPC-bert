# MRPC-bert

This model is a fine-tuned version of [bert-base-uncased](https://huggingface.co/bert-base-uncased) on the GLUE MRPC dataset.
Model link : [https://huggingface.co/brianhuster/MRPC-bert/](https://huggingface.co/brianhuster/MRPC-bert/)

### Training hyperparameters

The following hyperparameters were used during training:
- num_epochs: 3

### Framework versions

- Transformers 4.38.0.dev0
- Pytorch 2.1.2
- Datasets 2.18.0
- Tokenizers 0.15.0

#Running model with Python
```
from transformers import pipeline

classifier = pipeline("text-classification", model="brianhuster/MRPC-bert")
classifier(
    "Sentence 1. Sentence 2."
)
```
Replace "Sentence 1" and "Sentence 2" with your actual input sentence. Each sentence should end with a fullstop, even if they are questions. The model will return LABEL_1 if they are are equivalent in meaning, LABEL_1 otherwise.
