# Document Summarizer and Q&A Application

This Streamlit application allows users to summarize documents and perform question-answering on PDFs. It leverages pre-trained language models from Hugging Face's `transformers` library to provide accurate and concise results. The application provides a user-friendly interface for uploading documents, asking questions, and generating summaries.

## Features

1. **Document Summarization**: Upload a PDF document and get a concise summary based on a provided prompt.
2. **Question Answering on PDFs**: Upload a PDF document, enter a question, and receive an answer based on the document's content.
3. **History Tracking**: View a history of questions asked and answers received.

## Installation

To run this application, ensure you have Python installed. Follow these steps to set up the environment:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo/document-summarizer-qa.git
    cd document-summarizer-qa
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Streamlit App**:
    ```bash
    streamlit run app.py
    ```

2. **Navigate the Interface**:
   - Use the sidebar to select either "Question Answering PDFs" or "Summarize Document".
   - Upload a PDF file.
   - For summarization, enter your prompt and optionally specify a maximum length for the summary.
   - For question answering, enter your question in the text area and click "Answer".

## Code Overview

### Dependencies

- **Streamlit**: For building the web application.
- **Transformers**: For utilizing pre-trained language models.
- **PyPDF2**: For extracting text from PDF documents.
- **LangChain**: For managing language model prompts and chains.

### Key Components

- **Text Summarization**:
  - The `text_summary` function generates summaries using a pre-trained T5 model.
  - The `spliter` function splits long texts into manageable chunks.

- **Question Answering**:
  - The `qapdf` function uses a DistilBERT model to answer questions based on the content of a PDF.

- **PDF Handling**:
  - The `extract_text_from_pdf` function extracts text from uploaded PDF files.
  - The `extract_integer` function extracts the first integer from a string, used to get the maximum summary length.

- **Streamlit Interface**:
  - The app's layout and styling are defined in the `st.markdown` section with custom CSS.
  - The main logic for handling user input and displaying results is within the `st.sidebar` and main content area.

## Customization

You can customize the models and the interface to fit your specific needs:
- Replace the pre-trained models with other models available on Hugging Face.
- Modify the CSS for a different look and feel.
- Extend the functionality by adding more features such as different file types or advanced NLP tasks.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you have any suggestions or improvements.

## License

This project is licensed under the MIT License.

---

By following these instructions, you should be able to set up and run the Document Summarizer and Q&A Application locally. Enjoy using the tool and feel free to contribute to its development!
