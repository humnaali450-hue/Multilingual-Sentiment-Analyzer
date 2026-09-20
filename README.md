# 🌐 Multilingual Sentiment Analyzer

An AI-powered web application that analyzes the **sentiment of text in multiple languages** using pretrained Transformer models. The application automatically detects the input language and classifies the text as **Positive, Negative, or Neutral**, along with a confidence score.

Built with **Python, Streamlit, Flask, Hugging Face Transformers, PyTorch, and LangDetect**.

---

## ✨ Features

* 🌐 **Multilingual Sentiment Analysis**
* 🧠 **Pretrained Transformer Models**
* 🔍 **Automatic Language Detection**
* 📊 **Prediction Confidence Score**
* ⚡ **Real-Time Sentiment Prediction**
* 🎨 **Interactive Streamlit Interface**
* 🔌 **Flask REST API Backend**
* 🤗 **Hugging Face Transformers Integration**
* 🐍 **Python-Based ML Pipeline**
* 📱 **User-Friendly Web Interface**

---

## 🏗️ Project Architecture

```text
User Input
    │
    ▼
Streamlit Web Interface
    │
    ▼
Language Detection
    │
    ▼
Flask API
    │
    ▼
Hugging Face Transformer Model
    │
    ▼
Sentiment Prediction
    │
    ├── Positive
    ├── Negative
    └── Neutral
    │
    ▼
Confidence Score
    │
    ▼
Result Display
```

---

## 🛠️ Tech Stack

| Technology                   | Purpose                      |
| ---------------------------- | ---------------------------- |
| 🐍 Python                    | Core programming language    |
| 🎨 Streamlit                 | Interactive web interface    |
| ⚙️ Flask                     | REST API backend             |
| 🤗 Hugging Face Transformers | Pretrained NLP models        |
| 🔥 PyTorch                   | Deep learning framework      |
| 🌐 LangDetect                | Automatic language detection |
| 📊 Pandas                    | Data processing              |
| 🔢 NumPy                     | Numerical operations         |

---

## 2️⃣ Create a Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Application

## Start Flask API

Open a terminal and run:

```bash
python app.py
```

The Flask API will start locally.

---

## Start Streamlit Application

Open another terminal and run:

```bash
streamlit run streamlit_app.py
```

The application will open in your browser.

Usually, Streamlit runs at:

```text
http://localhost:8501
```

---

# 💡 How It Works

The application follows a simple NLP pipeline:

### Step 1 — User Input

The user enters text into the Streamlit interface.

Example:

```text
I really enjoyed this movie. It was amazing!
```

### Step 2 — Language Detection

The application automatically identifies the language using **LangDetect**.

Example:

```text
Detected Language: English
```

### Step 3 — Transformer Model

The text is processed using a pretrained Transformer-based sentiment analysis model.

### Step 4 — Sentiment Classification

The model predicts one of the following categories:

```text
Positive
Negative
Neutral
```

### Step 5 — Confidence Score

The application displays the model's confidence for the prediction.

Example:

```text
Sentiment: Positive
Confidence: 96.42%
```

---

# 🌍 Multilingual Support

The application is designed to analyze text written in multiple languages.

Example inputs:

| Language     | Example                       |
| ------------ | ----------------------------- |
| 🇬🇧 English | `I love this product!`        |
| 🇫🇷 French  | `J'adore ce produit !`        |
| 🇪🇸 Spanish | `Me encanta este producto.`   |
| 🇩🇪 German  | `Ich liebe dieses Produkt.`   |
| 🇮🇹 Italian | `Adoro questo prodotto.`      |
| 🇵🇰 Urdu    | `مجھے یہ پروڈکٹ بہت پسند ہے۔` |

> Supported languages depend on the pretrained model and language-detection configuration used in the project.

---

# 🔌 API Usage

The Flask backend exposes an API endpoint for sentiment prediction.

### Endpoint

```text
POST /predict
```

### Example Request

```json
{
    "text": "I really love this application!"
}
```

### Example Response

```json
{
    "sentiment": "Positive",
    "confidence": 0.96
}
```

---

# 📊 Example Predictions

| Input                              | Sentiment   | Confidence |
| ---------------------------------- | ----------- | ---------: |
| `I absolutely love this product!`  | 🟢 Positive |        98% |
| `This is the worst experience.`    | 🔴 Negative |        97% |
| `The product was delivered today.` | ⚪ Neutral   |        89% |

*Confidence values are illustrative and may vary depending on the model.*

---

# 🧠 Machine Learning Approach

The application uses **pretrained Transformer-based NLP models** rather than training a sentiment classifier from scratch.

### Pipeline

```text
Input Text
     ↓
Language Detection
     ↓
Text Preprocessing
     ↓
Transformer Tokenization
     ↓
Pretrained Transformer Model
     ↓
Sentiment Classification
     ↓
Confidence Score
```

This approach allows the application to take advantage of representations learned from large-scale language datasets.

---

# 📦 Requirements

Main dependencies include:

```text
streamlit
flask
transformers
torch
langdetect
pandas
numpy
```

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

# 🔐 Environment Variables

If your implementation requires API keys or configuration values, create a `.env` file:

```text
API_KEY=your_api_key
```

Never commit sensitive credentials to GitHub.

Add the following to `.gitignore`:

```text
.env
venv/
__pycache__/
*.pyc
```

---

# 🎯 Use Cases

This application can be used for:

* 📱 Social media sentiment analysis
* ⭐ Customer review analysis
* 🛍️ Product feedback analysis
* 💬 Customer support analytics
* 📊 Brand monitoring
* 📰 Opinion mining
* 🌍 Multilingual feedback analysis
* 📈 Business intelligence

---

# 🧪 Testing

Run the application and test it with different languages and sentiment types
