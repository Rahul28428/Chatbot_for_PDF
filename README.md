# Chatbot_for_PDF

## Overview
Chatbot_for_PDF is a conversational AI chatbot designed to answer questions about a wine business using a provided corpus. It is optimized to answer questions based on the given text data, and if a user asks a question outside of the corpus, it will direct them to contact the business directly. This chatbot is built with LangChain, Streamlit, and Google Generative AI.

## Features
- Minimalistic UI for user interaction
- Ability to answer questions from a specified corpus
- Redirect users to contact the business for out-of-corpus questions
- Maintains conversation history for context-aware responses
- Optimized for low latency and cost-effective usage

## Setup Instructions
### Prerequisites
- Python 3.8 or higher
- Google API Key for Google Generative AI

### Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/Rahul28428/Chatbot_for_PDF.git
    cd Chatbot_for_PDF
    ```

2. Create and activate a virtual environment: (Optional)
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

4. Set up environment variables:
    Create a `.env` file in the root directory and add your Google API key:
    ```env
    GOOGLE_API_KEY=your_google_api_key
    ```

### Running the Application
1. Run the Streamlit application:
    ```bash
    streamlit run main.py
    ```

2. Upload your PDF files through the sidebar and start asking questions.

### Usage
1. Upload PDF documents that contain the corpus of wine-related information.
2. Click "Submit & Process" to process the uploaded files.
3. Use the chat interface to ask questions about the wine business.
4. The chatbot will provide answers based on the uploaded documents and maintain the conversation context for follow-up questions.

## Project Structure
- `main.py`: The main application script.
- `requirements.txt`: List of dependencies.
- `.env`: Environment variables file (not included, needs to be created).

## Technical Details
### Libraries and Tools Used
- **Streamlit**: For creating the web UI.
- **LangChain**: For building conversational chains and handling QA.
- **FAISS**: For efficient similarity search in vector embeddings.
- **Google Generative AI**: For embeddings and conversational model.
- **PyPDF2**: For extracting text from PDF files.

### Approach
1. **Text Extraction**: Extract text from uploaded PDFs.
2. **Text Chunking**: Split extracted text into manageable chunks.
3. **Vector Store**: Create and store vector embeddings using FAISS.
4. **Conversational Chain**: Load a QA chain with memory for context-aware responses.
5. **User Interaction**: Handle user inputs and generate responses based on the corpus.

### Challenges and Solutions
- **Challenge**: Ensuring accurate context handling in conversation.
  - **Solution**: Used LangChain's `ConversationBufferMemory` to maintain chat history.
- **Challenge**: Reducing latency and API costs.
  - **Solution**: Optimized text chunking and embeddings, used efficient search with FAISS.

### Future Scope
- Integrate more advanced conversational features.
- Add multi-language support.
- Improve UI/UX for better user interaction.
- Implement more sophisticated error handling and fallback mechanisms.

## Demo
<a href="https://www.loom.com/share/4611d07dda3446dc930d0af2cd3c13bd?sid=7a06e957-f52f-47aa-afc7-a73bb567f01d"> Link </a>

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
