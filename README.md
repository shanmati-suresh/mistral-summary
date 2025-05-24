# PDF Summarizer using Mistral-7B-Instruct

This Python script extracts text from a PDF file and generates a summary using the Mistral-7B-Instruct-v0.3 language model via the Hugging Face Transformers library.

---

## 🔐 Hugging Face Token Setup

To access models like `mistralai/Mistral-7B-Instruct-v0.3`, you may need to authenticate with Hugging Face using a personal access token.

### Steps to Request and Use Your Hugging Face Token:

1. **Create a Hugging Face account**
   Go to [https://huggingface.co/join](https://huggingface.co/join) and sign up if you don’t already have an account.

2. **Generate an access token**

   * Visit [https://huggingface.co/settings/tokens](https://huggingface.co/settings/tokens)
   * Click on **"New token"**
   * Choose **"Read"** role
   * Give it a name (e.g., `pdf-summarizer`)
   * Click **Generate token**

3. **Login using the token**
   You can authenticate your script by uncommenting and adding your token:

   ```python
   from huggingface_hub import login
   login(token="your_token_here")
   ```

---

## ⚙️ How the Code Works

This script automates the process of summarizing PDF content using an advanced AI model:

1. **Text Extraction**
   The script reads the PDF file using `PdfReader` and extracts text from each page.

2. **Model Loading**
   The `mistralai/Mistral-7B-Instruct-v0.3` model is loaded using the Hugging Face Transformers library. This model is specifically trained to follow instructions like summarization.

3. **Summarization Process**
   The script constructs a prompt by appending the extracted text to the instruction "Summarize the following:" and feeds it to the model. The model then generates a concise summary based on the input text.

4. **Output**
   The resulting summary is decoded and printed to the console.

---

## 🤖 What Mistral AI Does Here

* **Mistral AI** provides the `Mistral-7B-Instruct-v0.3` model, an open-weight large language model fine-tuned to follow human instructions.
* In this script, Mistral AI's model is responsible for:

  * Understanding natural language instructions.
  * Processing the extracted PDF content.
  * Generating a human-like summary that captures the core ideas of the document.
* The model uses its deep learning architecture to interpret and condense lengthy text input into a coherent summary.

---

## 🏃 How to Run

1. Install required packages:

   ```bash
   pip install transformers pypdf huggingface_hub
   ```

2. Run the script:

   ```bash
   python pdf_summarizer.py
   ```

3. Make sure to set your PDF path inside the script:

   ```python
   pdf_path = "/path/to/your/file.pdf"
   ```

---

## 📁 Notes

* This script currently processes only up to 4000 characters of text.
* Mistral models are available under permissive licenses but may require a Hugging Face token.


