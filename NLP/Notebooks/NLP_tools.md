
# NLP Tools


##  Introduction

Besides **NLTK**, other powerful NLP libraries include:
- **spaCy**
- **Gensim**

Let’s explore both in detail.

---

## 1. spaCy

A modern NLP library for **production use** — fast and object-oriented.

### Key Features

- Tokenization  
- Lemmatization  
- POS Tagging  
- Named Entity Recognition (NER)  
- Text Classification  
- Dependency Parsing 

### Installation

```bash
pip install -U spacy
```

To install a model:

```bash
python -m spacy download en_core_web_sm
```

### Models

spaCy models follow this format:  
`[lang]_[genre]_[size]` → e.g., `en_core_web_sm`

- **Type**: `core`, `depent`  
- **Genre**: `web`, `news`, etc.  
- **Size**: `sm`, `md`, `lg`

### Loading a Model

```python
import spacy
model = spacy.load("en_core_web_sm")
```

### Example Usage

```python
text = "I bought a pair of watch for Tom and Elizabeth which costs $50 each."
processed = model(text)

for token in processed:
    print(f"{token.text} -- {token.pos_}")
```

### POS Hashing

```python
for token in processed:
    print(f"{token.text} -- {token.pos_} -- {token.pos}")
```

### Pipeline Components

spaCy's NLP pipeline includes:

```python
model.pipe_names
# Output: ['tagger', 'parser', 'ner']
```

You can disable components:

```python
model.disable_pipes('parser', 'ner')
```

---

## 2. Gensim

An open-source library for:
- Word vector modeling
- Unsupervised topic modeling
- Document similarity

### Installation

```bash
pip install -U gensim
```

### Key Concepts

- **Document**: A single text (e.g., article)  
- **Corpus**: Collection of documents  
- **Dictionary**: Maps words to unique IDs  
- **Vector**: Bag-of-Words representation  
- **Model**: Transform vectors (e.g., TF-IDF)

### Example: Dictionary

```python
from gensim.corpora import Dictionary

document = ["Tomorrow Tom and Elizabeth are getting married...",
            "I bought a pair of watch for Tom and Elizabeth..."]

tokens = [[token for token in docs.split()] for docs in document]
dictionary = Dictionary(tokens)
print(dictionary.token2id)
```

### Example: Vector

```python
new_document = "I hope they like my gift"
vector = dictionary.doc2bow(new_document.lower().split())
print(vector)
# Output: [(10, 1)] where 10 = 'gift'
```

### TF-IDF Example

```python
from gensim import models
import numpy

documents = ['This is first line', 'These are second lines', 'This is third line']
tokens = [[token for token in docs.split()] for docs in documents]
dictionary = Dictionary(tokens)
vector = [dictionary.doc2bow(token) for token in tokens]

tfidf = models.TfidfModel(vector)

for document in tfidf[vector]:
    print([[dictionary[id], numpy.around(freq, decimals=3)] for id, freq in document])
```

---

## 3. 🤗 Huggingface Transformers (Overview)

- Provides SOTA architectures:
  - **BERT**, **RoBERTa**, **DistilBERT**, **XLNet**, etc.
- Useful for:
  - Summarization  
  - Question Answering  
  - Machine Translation  
  - Language Generation  

Explore: [https://huggingface.co/transformers](https://huggingface.co/transformers)
