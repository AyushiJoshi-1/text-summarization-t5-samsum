\# Text Summarization using Hugging Face Transformers



\## Overview



This project is an NLP-based text summarization application built using a fine-tuned T5 Transformer model from Hugging Face.



The model is trained on the SAMSum dataset to generate concise summaries from dialogue and conversational text.



The application integrates a FastAPI backend with an HTML frontend, allowing users to input text and receive automatically generated summaries.



\## Features



\- Dialogue summarization using a fine-tuned T5 Transformer

\- Text preprocessing and tokenization

\- Deep learning-based summary generation

\- FastAPI backend for handling summarization requests

\- Interactive HTML frontend

\- Support for CPU, CUDA, and Apple Silicon (MPS) devices



\## Technologies Used



\- Python

\- Hugging Face Transformers

\- T5 (Text-to-Text Transfer Transformer)

\- PyTorch

\- Pandas

\- FastAPI

\- HTML

\- CSS

\- JavaScript



\## Dataset



This project uses the \*\*SAMSum dataset\*\*, which contains conversational dialogues along with their human-written summaries.



The dataset is divided into three parts:



\- Training dataset

\- Validation dataset

\- Testing dataset



These datasets are used for model training, validation, and evaluation.



\## Model



The project uses the pretrained `t5-small` Transformer model, fine-tuned for dialogue summarization.



The model processes conversational text and generates a concise summary while preserving the main information.



\## Project Workflow



1\. Load the SAMSum dataset.

2\. Preprocess dialogue and summary text.

3\. Tokenize the input dialogues and target summaries.

4\. Fine-tune the pretrained T5 model.

5\. Save the trained model and tokenizer.

6\. Load the saved model for inference.

7\. Generate summaries from user-provided text.

8\. Display the generated summary through the web application.



\## Project Structure



```text

text-summarization-huggingface/

│

├── app.py

├── index.html

├── text\_summarizer.ipynb

├── requirements.txt

├── README.md

├── .gitignore

│

├── data/

│   ├── samsum-train.csv

│   ├── samsum-test.csv

│   └── samsum-validation.csv

│

└── saved\_summary\_model/

&#x20;   └── Fine-tuned T5 model and tokenizer files

```



\## Installation



\### 1. Clone the repository



```bash

git clone https://github.com/AyushiJoshi-1/text-summarization-huggingface.git

```



\### 2. Navigate to the project directory



```bash

cd text-summarization-huggingface

```



\### 3. Create a virtual environment



```bash

python -m venv venv

```



\### 4. Activate the virtual environment



For Windows:



```bash

venv\\Scripts\\activate

```



\### 5. Install dependencies



```bash

pip install -r requirements.txt

```



\## Run the Application



Start the FastAPI server using:



```bash

uvicorn app:app --reload

```



Open the following URL in your browser:



```text

http://127.0.0.1:8000

```



Enter your dialogue or text in the input field and click the \*\*Summarize\*\* button to generate a summary.



\## API Endpoint



The application provides the following API endpoint:



\### POST `/summarize/`



Accepts dialogue text and returns a generated summary.



Example request:



```json

{

&#x20; "dialogue": "Enter your dialogue or text here."

}

```



Example response:



```json

{

&#x20; "summary": "Generated summary of the input text."

}

```



\## Future Improvements



\- Evaluate summarization performance using ROUGE metrics

\- Improve the user interface and user experience

\- Support longer input texts

\- Deploy the application to a cloud platform

\- Optimize inference performance



\## Author



AYUSHI JOSHI



