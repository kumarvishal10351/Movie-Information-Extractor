# 🎬 Movie Information Extractor

A simple AI-powered web app built with **Streamlit** and **LangChain** that extracts structured movie information from unstructured text using a **Mistral model**.

---

## 🚀 Features

* Convert raw movie descriptions into structured data
* Uses **Pydantic schema** for reliable output formatting
* Displays both:

  * Raw model output
  * Clean structured JSON
* Simple and interactive UI with Streamlit
* Fast and lightweight setup

---

## 🧠 How It Works

1. User inputs a paragraph describing a movie
2. A prompt is constructed with formatting instructions
3. The Mistral model processes the input
4. Output is parsed into a structured format using `PydanticOutputParser`
5. Results are displayed in the UI

---

## 📦 Tech Stack

* **Python**
* **Streamlit** – UI framework
* **LangChain** – LLM orchestration
* **Mistral AI** – Language model
* **Pydantic** – Data validation & schema

---

## 📁 Project Structure

```
project/
│── app.py
│── requirements.txt
│── .env
│── README.md
```

---

## ⚙️ Installation

1. Clone the repository:

```bash
git clone <your-repo-url>
cd <your-project-folder>
```

2. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate  # (Linux/Mac)
venv\Scripts\activate     # (Windows)
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the root directory:

```
MISTRAL_API_KEY=your_api_key_here
```

> ⚠️ Never share your API keys publicly.

---

## ▶️ Run the App

```bash
streamlit run app.py
```

---

## 📌 Example Input

```
Inception is a 2010 science fiction film directed by Christopher Nolan, starring Leonardo DiCaprio...
```

---

## 📤 Example Output

```json
{
  "title": "Inception",
  "release_year": 2010,
  "genre": ["Science Fiction"],
  "director": "Christopher Nolan",
  "cast": ["Leonardo DiCaprio"],
  "rating": null,
  "summary": "A thief who steals corporate secrets through dream-sharing technology..."
}
```

---

## ⚠️ Notes

* The model may occasionally fail to follow the schema exactly
* Error handling is included to catch parsing issues
* Best results come from well-written descriptive paragraphs

---

## 🔮 Future Improvements

* Add support for multiple models (OpenAI, Groq, etc.)
* Export structured data (CSV/JSON download)
* Add batch processing
* Improve UI/UX

---

## 🤝 Contributing

Feel free to fork the repo and submit pull requests.

---

## 📜 License

This project is open-source and available under the MIT License.
