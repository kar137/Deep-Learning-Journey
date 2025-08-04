# Natural Language Processing (NLP) Introduction

---

## Introduction to NLP

Natural Language Processing (NLP) is a field at the intersection of computer science, linguistics, and AI that enables communication between humans and machines using natural language.

Common NLP applications: **Google Search**, **Alexa**, **Siri**, **Google Assistant**, **Chatbots**.

---

## Human Language vs Machine Understanding

- **Human Language**: Tool for expressing ideas via written/spoken words, gestures, signs.
- Unique trait: **Compositionality** – the ability to create infinite sentences with limited vocabulary.
- Animals use symbols/sounds, but human language is far more complex.

---

## What is NLP?

- NLP enables machines to understand, interpret, and generate human language.
- Focuses on **information extraction** from human input and producing understandable output.
- NLP draws from:
  - Linguistics
  - Artificial Intelligence
  - Computer Science

---

## Brief History of NLP

| Year | Event |
|------|-------|
| 1950 | Alan Turing proposes the **Turing Test** |
| 1954 | **Machine Translation** experiments begin (Russian ↔ English) |
| 1960 | Contributions by **Noam Chomsky** to linguistics |
| 1980s | Shift from rule-based to **probabilistic models** |
| 2000+ | **Deep Learning dominates** NLP research due to data explosion |

---

## Why NLP?

- Human language ≠ Machine language.
- NLP **bridges the gap** between human communication and computer understanding.
- Enables processing of vast textual data available on the web.

---

## Why is NLP Difficult?

- Human language is:
  - **Ambiguous**
  - **Contextual**
  - Constantly **evolving**
- Challenges:
  - **Multiple interpretations** (semantic, syntactic, pragmatic)
  - **Background knowledge** required (e.g., “it” in a sentence)
  - Influence of **demographics, dialects, slang, sarcasm**, etc.

---

## Types of Ambiguity in Language

| Type                | Description | Example |
|---------------------|-------------|---------|
| **Phonological**    | Words sound the same | *Eye* vs *I*, *No* vs *Know* |
| **Lexical**         | One word, multiple meanings | *Bank*: River bank or financial institution |
| **Syntactic**       | Ambiguity from sentence structure | *The tourist saw the child with a telescope* |
| **Semantic**        | Uncertainty in sentence meaning | *Mark and Elizabeth got married last week* |
| **Pragmatic**       | Depends on context & speaker's intention | *I love chicken* (food vs animal) |

### How to Handle Ambiguity

To address ambiguity:
- Use **world knowledge** and **context**.
- Perform multiple levels of language analysis:
  - Morphological
  - Syntactic
  - Semantic
  - Pragmatic

---

## Multidisciplinary Nature of NLP

NLP is not only technical but also social, cognitive, and linguistic in nature:

| Field               | Role in NLP |
|---------------------|-------------|
| **Linguistics**     | Structure of words and sentences |
| **Psycholinguistics** | How humans comprehend language |
| **Cognitive Modeling** | Computational models of language |
| **Philosophy**      | Semantics and world knowledge |
| **Computer Science** | Implementation of NLP algorithms |
| **Artificial Intelligence** | Reasoning, inference, knowledge representation |
| **Statistics**      | Probabilistic models (e.g., N-grams) |
| **Machine Learning** | Learn patterns, automate decision-making |


# Domains of Natural Language Processing (NLP)

---

##  Overview

We previously explored the **multidisciplinary fields** involved in NLP. In this section, we’ll dive into **NLP domains** that define specific **use cases** and tasks. Though domains are categorized by core functionality, they are interconnected—except for the high-level separation into **Text Domain** and **Speech Domain**.

---

## 1. Text Representation and Classification

This is one of the **most fundamental and widely used domains** in NLP. It deals with **full-textual data**, ranging from short tweets to large book corpora, and involves models that classify the content into predefined categories.

### Text Representation

Text representation is the process of converting text into **numerical features** that ML/DL models can process.

**Example: Bag of Words (BoW)**

- Create a vocabulary of all unique words.
- Represent each text sample using binary (1 if word is present, 0 if not).

Other common methods:
- **TF-IDF Vectorization**
- **ASCII or Unicode Encoding**
- **Word Embeddings (e.g., Word2Vec, GloVe)**

> Good features = Good models. Poor feature engineering leads to poor performance.

###  Text Classification

Once text is represented numerically, a model can be trained to **predict categories/labels** for the input.

- Input: Word representation (e.g., BoW or TF-IDF vectors)
- Output: Predicted class or category

It is widely used in:
- **Spam detection**
- **Sentiment analysis**
- **News categorization**

---

## 2. Information Retrieval

This domain focuses on extracting **key insights** from **unstructured data** (text, speech, or image).

### Common Applications:
- Keyword or tag extraction
- Named Entity Recognition (NER)
- Customer feedback intent extraction
- Document summarization
- Question answering systems

Example: Automatically filling in a **structured template** from a **news article** using extracted information.

---

## 3. Conversational Agents

This domain powers **dialogue systems** like:
- Chatbots
- Voice assistants (e.g., Alexa, Siri)

These systems conduct conversations in natural language by:

1. Accepting user input (text or speech)
2. Processing the input using NLP models
3. Generating and delivering a human-like response

> Speech-based inputs are often converted to text for processing, then converted back to speech for output (if needed).

### Advancements

Thanks to ML/DL, modern conversational agents:
- Are more **intelligent and responsive**
- Can be used across industries:
  - **Retail**: Customer support bots
  - **Media**: News delivery bots
  - **Healthcare**: Symptom checkers, virtual nurses



# NLP Applications

---

### 1. Spam Classification
- **Domain**: Text classification  
- **Use Case**: Detect spam emails (e.g., Gmail spam filter)  
- **Features used**: Subject, sender address, suspicious keywords, historical patterns  
- **Techniques**: BoW, TF-IDF, ML classifiers

---

### 2. Personal Assistants
- Examples: **Google Assistant**, **Siri**, **Cortana**  
- **Function**: Understand and respond to voice/text commands  
- **Tasks**: Reminders, search, scheduling, etc.  
- **Underlying tech**: ASR + NLP + TTS

---

### 3. Search Engines
- **Autocomplete** & **Spell correction** via NLP  
- **Query understanding** for better relevance  
- **Page ranking** (with NLP-based content analysis)  
- Example: Google’s predictive search

---

### 4. Machine Translation
- Converts source language to target language  
- Examples: Google Translate, DeepL  
- Can include **OCR + Translation** for text in images  
- **Models**: Seq2Seq, Transformers (e.g., MarianMT, mBART)

---

### 5. Spelling & Grammar Correction
- Tools: **Grammarly**, **MS Word grammar check**  
- Fixes grammatical and spelling mistakes in real-time  
- Models: Language models (e.g., BERT, GPT) + Rule-based checks

---

## Industry-Specific Applications

### 6. Social Media Analysis
**Common Tasks**:
- **Sentiment analysis**: Understand user opinion (positive/neutral/negative)
- **Opinion mining**: Extract feedback/opinions for market insight
- **Trending topic detection**: Google Trends, hashtags
- **Fake news detection**: Detect misinformation
- **Content filtering**: Block inappropriate or harmful content

---

### 7. Retail Catalog Extraction
**Goals**:
- Clean and structured product descriptions
- Enable **smart search** and **recommendations**
- Personalization: Recommend based on inferred user interests  
**Applications**:
- **Review analysis**
- **Product search**
- **Product recommendation**

---

### 8. Healthcare & Health Records Analysis
- Extract insights from **unstructured data** (notes, prescriptions, etc.)
- Applications:
  - **Patient triage** & billing
  - **Clinical info extraction**
  - **Medical assistants** (FAQs, scheduling bots)
- Improves **efficiency** and **accuracy** in healthcare workflows

---

### 9. Text Generation & Completion
- **Natural Language Generation (NLG)**  
- Input: Prompt → Output: Autocompleted content (e.g., story, reply)  
- Tools: GPT, T5, etc.

**Example**:  
Prompt: *"I was just sitting in my room and..."*  
→ Model completes with a story using learned language patterns.
