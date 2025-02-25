# Text Summarization and Translation using Transformers

This project demonstrates how to use **T5** for text summarization and **MarianMT** for text translation. It allows users to:
1. Summarize text using the T5 model.
2. Translate text using the MarianMT model.
3. Summarize and then translate text.

The code is designed to run in **Google Colab** and supports uploading text files for processing.

---

## Features
- **Text Summarization**: Summarize long text using the `t5-large` model.
- **Text Translation**: Translate text to a target language using MarianMT models.
- **Summarization + Translation**: Summarize text and then translate the summary.

---

## Setup

### 1. Requirements
- Python 3.x
- Google Colab (or a local environment with GPU support)
- Required Python libraries:
  ```bash
  pip install torch transformers
  ```

### 2. Google Colab Setup
1. Open Google Colab: [https://colab.research.google.com/](https://colab.research.google.com/).
2. Upload the script or copy and paste the code into a new notebook.
3. Ensure you are using a GPU:
   - Go to `Runtime` > `Change runtime type` > Select `GPU` under Hardware accelerator.

---

## Usage

### 1. Running the Script
1. Run the script in Google Colab.
2. Choose a task:
   - **1**: Summarization
   - **2**: Translation
   - **3**: Summarization + Translation
3. Upload a text file when prompted.
4. View the results.

### 2. Example Input
- **Text File**: Upload a `.txt` file containing the text you want to process.
- **Target Language**: For translation tasks, specify the target language (e.g., `fr` for French, `de` for German, `ar` for Arabic).

### 3. Example Output
- **Summarization**:
  ```plaintext
  Original Text:
  This is a long text that needs to be summarized...

  Summarized Text:
  This is a summary of the long text.
  ```

- **Translation**:
  ```plaintext
  Original Text:
  This is a text that needs to be translated...

  Translated Text (fr):
  Ceci est un texte qui doit être traduit...
  ```

- **Summarization + Translation**:
  ```plaintext
  Original Text:
  This is a long text that needs to be summarized and translated...

  Summarized Text:
  This is a summary of the long text.

  Translated Summary (ar):
  هذا ملخص للنص الطويل.
  ```

---

## Code Overview

### 1. Summarization
- Uses the **T5 model** (`t5-large`) for high-quality text summarization or (`t5-small`) for lightweight summarization.
- The input text is prefixed with `"summarize: "` to indicate the task.
- The model generates a concise summary.

### 2. Translation
- Uses the **MarianMT model** for translation.
- Supports multiple languages (e.g., French, German, Arabic).
- The target language is specified by the user.

### 3. Summarization + Translation
- Combines the summarization and translation tasks.
- First, the text is summarized using T5.
- Then, the summary is translated using MarianMT.

---

## Supported Languages for Translation
The MarianMT model supports translation between many languages. Some common language codes are:
- French (`fr`)
- German (`de`)
- Spanish (`es`)
- Arabic (`ar`)
- Chinese (`zh`)
- Russian (`ru`)

For a full list of supported languages, refer to the [Helsinki-NLP Opus-MT GitHub repository](https://github.com/Helsinki-NLP/Opus-MT).

---

## Limitations
- The summarization model (`t5-large`) produces higher-quality summaries but requires more computational resources (e.g., GPU memory and processing power).
- Translation quality depends on the MarianMT model and the target language.
- Large input texts may be truncated due to the model's maximum input length (512 tokens).

---


## Contact
- **Author**: Samoua Alsamoua
- **GitHub**: [samoua-alsamoua](https://github.com/samoua-alsamoua)
- **Website**: [saalsamoua.github.io](https://samoua-alsamoua.github.io/saalsamoua/)
