
# MultiPDF Chat App

> You can find the tutorial for this project on [YouTube](https://youtu.be/dXxQ0LR-3Hg).

## Introduction
------------
The MultiPDF Chat App is a Python application that allows users to chat with multiple PDF documents. Ask questions about the PDFs using natural language, and the application will provide relevant responses based on the content of the documents. The app now integrates with Azure OpenAI, leveraging its capabilities to generate accurate answers to your queries. Please note that the app will only respond to questions related to the loaded PDFs.

## How It Works
------------

![MultiPDF Chat App Diagram](./docs/PDF-LangChain.jpg)

The application follows these steps to provide responses to your questions:

1. **PDF Loading**: The app reads multiple PDF documents and extracts their text content.

2. **Text Chunking**: The extracted text is divided into smaller chunks for more effective processing.

3. **Language Model Integration**: Through Azure OpenAI, the application generates vector representations (embeddings) of the text chunks.

4. **Similarity Matching**: When you pose a question, the app compares it with the text chunks to find the most semantically similar ones.

5. **Response Generation**: The identified chunks are then processed by the Azure OpenAI model, which crafts a response based on the relevant PDF content.

## Dependencies and Installation
----------------------------
To install the MultiPDF Chat App, follow these steps:

1. Clone the repository to your local machine.

2. Install the necessary dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Set up the OpenAI integration with Azure by filling in the required fields in the `.env` file:
```commandline
OPENAI_API_KEY=your_openai_api_key
OPENAI_API_TYPE=azure
OPENAI_API_VERSION=your_openai_version
OPENAI_API_BASE=your_openai_base_url
```

## Usage
-----
To get started with the MultiPDF Chat App:

1. Ensure all dependencies are installed and the OpenAI details are set in the `.env` file.

2. Launch the app using the Streamlit CLI:
   ```
   streamlit run app.py
   ```

3. Your default web browser will open to display the app interface.

4. Upload multiple PDF documents as directed.

5. Use the chat interface to pose questions related to the uploaded PDFs.

## Contributing
------------
For educational purposes, this repository does not accept further contributions. It's supplemental material for a YouTube tutorial on building the project. However, feel free to use and modify the app as you see fit.

## License
-------
The MultiPDF Chat App is under the [MIT License](https://opensource.org/licenses/MIT).
