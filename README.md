## Documentation for Skillsense Web

<img width="960" alt="skillsense" src="https://github.com/Thirumurugan-12/Skillsense/assets/76591903/5ffc41bc-6717-4a90-ac68-da93033dc2e5">


### Introduction
Skillsense Web is a web application that provides language processing and information retrieval capabilities. It allows users to provide input in the form of web links, PDF files, or YouTube video transcripts. The application processes the input data, extracts information, and offers features such as summarization, translation, and even text-to-speech conversion.

### Code Components

1. **Import Statements**: The code starts with import statements that bring in various libraries and modules necessary for the application.

2. **Supported Languages**: A dictionary `supported_languages` is defined, which maps language codes to their corresponding human-readable names.

3. **Google Cloud Credentials**: The code sets the Google Application Credentials using the environment variable, allowing access to Google Cloud services such as DocumentAI, Translate, and Text-to-Speech.

4. **Streamlit Setup**: The Streamlit application is set up with the title "Skillsense Web." Users can interact with the application through a chat-like interface in the main section and configure options in the sidebar.

5. **VertexAI Initialization**: The VertexAI client is initialized with project and location information.

6. **Language Model (LLM) and Embeddings**: The code initializes the OpenAI language model (LLM) and VertexAI embeddings for text processing.

7. **Web Scraping**: A function `get_text(url)` is defined for web scraping, which extracts text content from a given URL and saves it to a temporary text file.

8. **Langchain Index Creation**: The code defines functions for creating Langchain indexes from text data, both for web content and PDF files. These indexes are used for efficient text retrieval.

9. **PDF to Text Conversion**: A function `pdf_to_text(path)` converts a PDF file to plain text using Google's DocumentAI.

10. **Text-to-Speech Conversion**: The `text_to_wav(voice_name, text)` function converts text into speech in WAV format using Google's Text-to-Speech service.

11. **Translation Function**: The `translating(text, lang)` function translates text to the specified language using Google's Translate service.

12. **Streamlit Sidebar and Options**: Users can choose from three input options: "link," "pdf," or "youtube." The sidebar allows users to provide input, select a language, and submit their choices.

13. **Processing Input**: The code processes the input based on the user's choice. For web links, it scrapes content, for PDF files, it converts them to text, and for YouTube, it retrieves video transcripts.

14. **Langchain Index Creation**: The code creates Langchain indexes for the processed text data.

15. **Querying**: Users can interact with the assistant by typing in the chat-like interface. The code processes user queries, retrieves responses, and translates them as needed.

16. **Smart Pod**: Users can select a language (Tamil or English) and listen to the generated text-to-speech audio.

17. **Chat History**: The code maintains a chat history, displaying user queries and assistant responses in a chat-like format.

### Instructions to Run the Code

1. Ensure you have the required libraries and dependencies installed. You may need to install them using `pip`. Here are some of the key dependencies:
   - Streamlit
   - Google Cloud libraries (DocumentAI, Translate, Text-to-Speech)
   - YouTube Transcript API
   - Beautiful Soup (for web scraping)

2. Set up Google Cloud credentials: You'll need to set your Google Application Credentials JSON file using the `os.environ["GOOGLE_APPLICATION_CREDENTIALS"]` line in the code. Make sure this file contains the necessary permissions for DocumentAI, Translate, and Text-to-Speech.

3. Run the application: Use the command `streamlit run your_script.py` to start the Streamlit application, replacing `your_script.py` with the name of the Python script containing your code.

4. Use the web application: Once the application is running, access it through a web browser. You'll see a sidebar with options to input a web link, PDF file, or YouTube video transcript. Select an option, provide input, choose a language, and submit your choices.

5. Interact with the assistant: You can interact with the assistant by typing queries in the chat-like interface. The code processes your queries, retrieves information, and displays responses. You can also listen to responses in the selected language using the "Smart Pod" feature.

6. Enjoy the language processing capabilities: The application offers summarization, translation, and text-to-speech features for various types of input data, making it a versatile tool for language processing and information retrieval.

That's it! You now have a fully functional Skillsense Web application that can process and provide information from different sources.
