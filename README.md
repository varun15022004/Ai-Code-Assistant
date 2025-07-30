
# 🧠 AI Code Assistant

AI Code Assistant is an intelligent application that reads coding questions from text or images and generates, executes, and explains Python solutions using large language models and OCR (Optical Character Recognition). It can be run via terminal or as a web application using Flask.

---

## 🚀 Features

* 🧾 **Text & Image Input**: Accepts direct text input or extracts problem descriptions from uploaded images using Tesseract OCR.
* 🧠 **AI Code Generation**: Utilizes the `LLaMA3-70B` model via Groq API to generate optimal Python code solutions.
* ⚙️ **Code Execution & Error Handling**: Runs the generated code in a secure E2B sandbox and explains any execution errors using the same AI model.
* 🌐 **Web Interface**: Simple, user-friendly web interface built using Flask.

---

## 📂 Project Structure

```bash
AI-Code-Assistant/
│
├── app.py            # Flask web app interface
├── main.py           # CLI script version
├── templates/
│   └── index.html    # HTML template for web interface
├── .env              # Environment variables (GROQ_API_KEY, E2B_API_KEY)
├── requirements.txt  # All dependencies
└── README.md         # Project documentation
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Ai-Code-Assistant.git
cd Ai-Code-Assistant
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Install [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)

> Ensure Tesseract is installed and the path is set correctly in `main.py` and `app.py`:

```python
pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"
```

---

## 🔐 API Keys

Create a `.env` file in the project root:

```bash
GROQ_API_KEY=your_groq_api_key
E2B_API_KEY=your_e2b_api_key
```

---

## 🖥️ Usage

### 1. Run from Terminal

```bash
python main.py
```

> Make sure `test_question.png` exists in the project directory.

### 2. Run Web App

```bash
python app.py
```

Visit: [http://localhost:5000](http://localhost:5000)
Upload an image **or** enter a problem description.

---

## 🧪 Sample

**Input** (Image/Text):

> "Write a Python function to find the factorial of a number."

**Output** (AI-generated):

```python
def factorial(n: int) -> int:
    if n == 0:
        return 1
    return n * factorial(n - 1)
```

✅ *Executed successfully with result for sample inputs.*

---

## 🛠️ Technologies Used

* **Python** 🐍
* **Flask** 🌐
* **Pytesseract (OCR)** 🔍
* **Groq API (LLaMA3)** 🧠
* **E2B Code Interpreter** ⚙️

---

## 📌 To Do

* [ ] Add file upload preview and result download options in web UI
* [ ] Support for multiple programming languages
* [ ] Dockerize for easier deployment

---

## 🤝 Contributing

Contributions are welcome! Please open issues and pull requests.

---

## 📃 License

MIT License © 2025 Varun Saini


