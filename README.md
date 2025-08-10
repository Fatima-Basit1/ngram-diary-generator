# N-Gram Language Modeling Approaches

This repository contains two different implementations aimed at the same task: building and evaluating n-gram language models on a Roman Urdu text dataset. Both approaches work toward similar goals but differ slightly in structure, feature set, and extra experimentation.

## Overview

The task involved:
- Preprocessing a text corpus (cleaning, tokenizing, and removing unnecessary characters).
- Training **unigram**, **bigram**, and **trigram** models.
- Exploring additional models like **backward bigram** and, in one approach, **bidirectional bigram**.
- Evaluating models based on **perplexity** to measure predictive accuracy.

While the core idea is similar, each implementation takes its own path in handling certain details, experimenting with additional models, and interpreting results.

---

## Approach 1

**Main Steps**
1. Load multiple text files and preprocess the data (lowercasing, removing numbers, tokenizing with NLTK).
2. Build unigram, bigram, and trigram models using the `ngrams` function.
3. Implement a backward bigram model (predicting the previous word from the next one).
4. Calculate probability distributions for each model.
5. Evaluate models with perplexity scores.

**Notable Points**
- More emphasis on exploring the backward bigram idea and how it differs from standard models.
- Highlights the challenges of reversed predictions in natural language.
- Discusses the trade-off between model complexity and data requirements.

---

## Approach 2

**Main Steps**
1. Load the Roman Urdu Diaries Corpus and clean it (remove numbers, tokenize words).
2. Train unigram, bigram, trigram, backward bigram, and **bidirectional bigram** models.
3. Use a `generatetext` function to produce sentences from each model.
4. Compute perplexity for each model to compare their accuracy.

**Notable Points**
- Includes bidirectional bigram generation in addition to backward bigram.
- Lists concrete perplexity results:
  - **Unigram:** 44.10
  - **Bigram:** 1.74
  - **Trigram:** 1.08
- Observes that trigram models produce the most coherent sentences, though they are more computationally expensive.

---

## Key Learnings from Both Approaches

- **Unigram models** are fast but lack contextual understanding.
- **Bigram models** add some context and perform much better.
- **Trigram models** capture even more context, resulting in the best perplexity scores, but require more computation and data.
- **Backward and bidirectional models** are interesting for research but generally less effective for natural forward-flowing text.
- Dataset quality and size strongly influence results.

---

## Getting Started

Clone this repository:

```bash
git clone https://github.com/yourusername/ngram-language-models.git
cd ngram-language-models
```
