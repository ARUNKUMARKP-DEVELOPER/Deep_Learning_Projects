# 🎓 University Chatbot using BERT

A BERT-powered intelligent chatbot that answers university-related queries by classifying user intents. Trained on a custom dataset of 38 distinct intents, this chatbot can respond to common student questions related to admissions, courses, fees, infrastructure, and more.

---

## 📂 Dataset

- **Source**: [Kaggle - Chatbot Dataset](https://www.kaggle.com/datasets/niraliivaghani/chatbot-dataset/data?select=intents.json)
- **Format**: `intents.json`
- **Size**: ~5KB
- **Structure**:
  - `tag`: Unique intent name (e.g., "greeting", "fees", "admission")
  - `patterns`: Example user inputs for each intent
  - `responses`: Predefined chatbot replies
  - `context_set/context_filter`: (optional) to control conversation flow
- **Total**: 405 user patterns mapped to 38 unique tags (intents)

---

## 🧠 Project Objective

To develop a university domain-specific chatbot capable of:
- Understanding student questions
- Classifying them into intents using BERT
- Responding intelligently using predefined responses
- Handling basic greetings, FAQ queries, and structured information

---

## 🛠️ Tech Stack

- **Language**: Python
- **Libraries**:
  - NLP: `nltk`, `wordcloud`, `transformers`, `bert`, `torch`
  - Data: `pandas`, `numpy`, `matplotlib`, `seaborn`, `missingno`
  - Modeling: `HuggingFace Transformers`, `BERT`, `Trainer API`, `Scikit-learn`, `Keras`
- **Model**: `bert-base-uncased` from HuggingFace Transformers
- **Training Framework**: `Trainer` with PyTorch backend
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1 Score

---

## 📊 Exploratory Data Analysis (EDA)

- Class Distribution of Intents (Tags)
- Word Frequency Analysis
- Word Cloud of User Patterns
- Text Statistics:
  - Average word length
  - Number of characters per input
  - Number of words per input

---

## 🧹 Preprocessing

- Tokenization using `nltk.word_tokenize`
- Stemming using `PorterStemmer`
- Stopword removal
- Label Encoding of intents
- Train-test split

---

## 🔍 Model Training

- **Model**: `BERTForSequenceClassification`
- **Tokenizer**: `BertTokenizer`
- **Max Sequence Length**: 256
- **Epochs**: 100
- **Batch Size**: 32 (train), 16 (eval)
- **Learning Rate Scheduler**: Warm-up steps & Weight decay
- **Trainer**: HuggingFace's `Trainer` API
- **Hardware**: Trained using CUDA (GPU)

---

## 🧪 Evaluation Results

| Metric      | Training Set | Test Set  |
|-------------|--------------|-----------|
| Accuracy    | 99.67%       | 92.15%    |
| F1 Score    | 99.85%       | 92.64%    |
| Precision   | 99.84%       | 94.09%    |
| Recall      | 99.86%       | 94.03%    |

---