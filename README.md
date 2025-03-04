# Urdu-to-English RNN Translator

This repository contains an implementation of a Recurrent Neural Network (RNN)-based model for translating Urdu text into English.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Preprocessing](#preprocessing)
- [Training](#training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Credits](#credits)

## Introduction
This project implements a sequence-to-sequence (Seq2Seq) model using an RNN-based approach for machine translation from Urdu to English. The model utilizes PyTorch and processes a dataset of parallel Urdu-English sentences.

## Dataset
The dataset consists of Urdu-English sentence pairs. It is preprocessed and divided into training, validation, and test sets. The dataset is expected to be stored in the `data/` directory with the following structure:
```
/data
  ├── eng.dev
  ├── urd.dev
  ├── eng.devtest
  ├── urd.devtest
```

## Model Architecture
The model follows a standard Encoder-Decoder architecture:
- **Encoder**: An RNN processes the input Urdu text and generates context vectors.
- **Decoder**: Another RNN takes the context vectors and generates English translations.
- **Attention Mechanism (if implemented)**: Helps the decoder focus on relevant parts of the input sequence during translation.

## Preprocessing
- Tokenization and cleaning of Urdu and English text.
- Vocabulary construction with a minimum frequency threshold.
- Encoding text into sequences of integer token IDs.
- Padding sequences to a uniform length for batch processing.
- Splitting data into training (70%), validation (15%), and test (15%) sets.

## Training
- Uses PyTorch’s `torch.utils.data.DataLoader` for batch training.
- Loss function: Cross-entropy loss.
- Optimizer: Adam optimizer with learning rate scheduling.
- Model trained on GPU if available.

## Evaluation
- The model is evaluated on the test set using BLEU score and accuracy.
- Translation quality is manually assessed by inspecting generated outputs.

## Results
The trained model achieves reasonable accuracy on the test set. BLEU scores and sample translations will be reported after training.

## Credits
This project was developed in collaboration with Ahmad Farhan. He can be reached via email at i211366@nu.edu.pk.


