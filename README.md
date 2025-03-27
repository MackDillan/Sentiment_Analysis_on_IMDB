# 🎬 Sentiment Analysis on IMDB Movie Reviews

## 🧠 Project Goal

Build a model that accurately classifies movie reviews as **positive** or **negative**.

---

## 📊 Dataset Overview

- **Source:** IMDB Movie Reviews  
- **Size:**  
  - 25,000 training examples  
  - 25,000 test examples  
- **Balanced Dataset:**  
  - 50% positive  
  - 50% negative  

**Exploratory Data Analysis includes:**
- Average and max length of reviews  
- Most frequent words (after removing stop-words)

---

## 🧼 Data Preprocessing & Augmentation

- **Text Cleaning:**  
  - Lowercasing  
  - Punctuation removal  
  - Tokenization  
  - Lemmatization

- **Data Augmentation:**  
  - Synonym replacement for richer training data

- **Sequence Preparation:**  
  - Tokenization  
  - Padding for uniform input length

---

## 🤖 Models

### 🔹 Baseline: SVM + TF-IDF

- **Vectorization:** TF-IDF with 10,000 features  
- **Preprocessing:** Stop-word removal, sparse matrix  
- **Classifier:** Linear SVM  
- **Accuracy:** `86.0%`

---

### 🔸 Advanced Model 1: LSTM with Attention

- **Architecture:**  
  `Embedding → LSTM → Attention → Dense → Dropout`  
- **Regularization:** L2 + Dropout  
- **Benefits:**  
  - Captures long-term dependencies  
  - Highlights important words with attention  
- **Accuracy:** `82.57%`

---

### 🔸 Advanced Model 2: GRU

- **Architecture:**  
  `Embedding → GRU → Dense → Dropout`  
- **Benefits:**  
  - Simplified model with strong performance  
- **Accuracy:** `86.3%`

---

### 🔸 Advanced Model 3: LSTM with Conv1D + BiLSTM

- **Architecture:**  
  `Embedding → BatchNorm → Conv1D → MaxPooling1D → Bidirectional LSTM → LSTM → Dropout → Dense`  
- **Regularization:** L2 + Dropout + BatchNorm  
- **Benefits:**  
  - Extracts both local and long-term features  
  - Highest accuracy and best generalization  
- **Accuracy:** `89.0%`

---

## 📈 Evaluation Metric

- **Primary Metric:** Accuracy

---

## ✅ Conclusion

- Data preprocessing is crucial for performance  
- LSTM with Conv1D and Bidirectional LSTM achieved the best results  
- Simpler models like GRU provided competitive performance with reduced complexity

---

## 🛠️ Technologies Used

- Python  
- Scikit-learn  
- TensorFlow / Keras  
- NumPy / Pandas /  
