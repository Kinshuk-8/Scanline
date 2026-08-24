# Scanline – Document Summarizer

Scanline is a simple browser-based document summarizer that extracts text from PDFs and images and generates a short summary along with key points.

🔗 **Live Demo:** https://unthinkable-document-summariser.netlify.app

## What it does

You can upload a PDF or an image of a document. The application extracts the text and gives you:

* A summary of the document
* Important key points
* The complete extracted text
* Word and sentence statistics

It also allows you to choose the summary length and copy or download the results.

## Features

| Feature         | Description                                                  |
| --------------- | ------------------------------------------------------------ |
| PDF Upload      | Extracts text from PDF files                                 |
| Image Upload    | Extracts text from JPG, PNG and WEBP images                  |
| OCR             | Uses Tesseract.js to read text from images                   |
| Summarization   | Generates an extractive summary based on important sentences |
| Summary Length  | Short, Medium and Long options                               |
| Key Points      | Shows the most relevant sentences                            |
| Copy            | Copy summary or extracted text                               |
| Download        | Download the summary as a `.txt` file                        |
| Drag & Drop     | Upload files by dragging them into the upload area           |
| Sample Document | Test the application without uploading a file                |
| File Limit      | Supports files up to 25 MB                                   |
| Privacy         | Files are processed in the browser                           |

## Technologies Used

| Technology   | Used For                        |
| ------------ | ------------------------------- |
| HTML         | Page structure                  |
| CSS          | UI design and responsive layout |
| JavaScript   | Application functionality       |
| PDF.js       | Extracting text from PDFs       |
| Tesseract.js | OCR for images                  |
| Netlify      | Hosting and deployment          |

## How it works

### 1. Upload

Upload a PDF or image, or drag and drop it into the upload area.

### 2. Text Extraction

For PDFs, the application uses **PDF.js** to extract the text.

For images, **Tesseract.js** is used for OCR.

### 3. Summarization

The extracted text is divided into sentences. The application checks the frequency of meaningful words in the document and gives each sentence a score.

The sentences with higher scores are selected for the summary and key points.

### 4. View Results

The application displays the summary, key points and the original extracted text side by side.

## Summary Options

| Option | Approx. amount of document used |
| ------ | ------------------------------: |
| Short  |                             12% |
| Medium |                             25% |
| Long   |                             40% |

The number of sentences is also limited so that the summary does not become unnecessarily long.

## Privacy

The application does not use a backend server for processing documents.

PDF extraction, OCR and summarization happen directly in the browser. This means the uploaded document is not sent to a server for processing.

## Project Structure

```text
Scanline/
│
├── index.html
└── README.md
```

The current project is built as a single HTML file containing the HTML, CSS and JavaScript code.

## Run Locally

Clone the repository:

```bash
git clone <your-repository-url>
cd Scanline
```

You can open `index.html` directly in a browser.

Or run it using a local server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deployment

The project is deployed on Netlify.

**Live:** https://unthinkable-document-summariser.netlify.app

## Future Improvements

* Support for more languages
* Better summarization using an AI/LLM model
* Support for more document formats
* PDF export for summaries
* Improved OCR for low-quality images
* Document history
* Search within extracted text

## Author

**Maddineni Kinshuk**
B.Tech Computer Science & Engineering
VIT-AP University
