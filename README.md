# 📚 Book Recommendation System using LLMs and Zero-Shot Classification

This project builds a smart **content-based book recommender** that suggests books based on their descriptions and genres using modern NLP techniques and large language models (LLMs). Built in Python using PyCharm and deployed via a simple interactive interface using Gradio.

---

## 🚀 Features

- ✅ Recommend books based on **semantic similarity** of descriptions
- ✅ Classify books as **Fiction** or **Nonfiction** using zero-shot classification
- ✅ Analyze book **emotions** using fine-tuned sentiment models
- ✅ Visual, real-time recommendation using a Gradio dashboard
- ✅ Uses a real-world dataset of 7K+ books from Kaggle

---

## 🧠 Technologies Used

| Tool/Library      | Purpose                             |
|------------------|-------------------------------------|
| Python 3.11       | Core programming language            |
| Pandas            | Data loading and preprocessing       |
| TF-IDF Vectorizer | Text-to-number transformation        |
| FAISS / LangChain | Vector search for similarity         |
| Hugging Face      | LLMs for classification & sentiment  |
| Transformers      | Pre-trained models like BART         |
| Gradio            | Web-based UI for interaction         |
| PyCharm           | IDE for development                  |

---

## 📁 Dataset

- **Source**: [7k Books with Metadata (Kaggle)](https://www.kaggle.com/datasets/dylanjcastillo/7k-books-with-metadata)
- Fields used: `title`, `subtitle`, `description`, `authors`, `categories`, `published_year`

---

## 🧪 How It Works

1. **Preprocessing**:
   - Cleans and filters book descriptions
   - Removes short/incomplete entries

2. **TF-IDF + Vector Search**:
   - Transforms text into vectors
   - Finds similar books using cosine similarity

3. **Zero-Shot Classification**:
   - Classifies books as "Fiction" or "Nonfiction" using `facebook/bart-large-mnli`

4. **Sentiment Analysis** *(optional)*:
   - Extracts emotional tone from book descriptions using LLMs

5. **Gradio UI**:
   - User inputs a query book
   - App recommends similar titles and shows classification

---

## 🛠️ Installation & Setup

```bash
# Clone the repository
git clone https://github.com/your-username/book-recommender.git
cd book-recommender

# Create a virtual environment (if not already)
python -m venv .venv
source .venv/bin/activate  # Mac/Linux
.venv\Scripts\activate     # Windows

# Install required packages
pip install -r requirements.txt

# Run the app (if using Gradio)
python app.py
