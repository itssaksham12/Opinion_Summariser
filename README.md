# Text Summarization with TextRank

This project implements a text summarization tool using the TextRank algorithm. It processes articles to generate concise summaries, leveraging natural language processing (NLP) techniques and various Python libraries.

## Project Overview

The project is structured as a Jupyter Notebook (`main.ipynb`) that performs the following tasks:

1. **Environment Setup**: Installs necessary Python packages using `pip` and imports them for use in the notebook.
2. **Data Loading**: Reads a CSV file containing articles into a Pandas DataFrame.
3. **Text Preprocessing**: Cleans and preprocesses the text data to prepare it for summarization.
4. **TextRank Algorithm**: Implements the TextRank algorithm to rank sentences based on their importance and generate a summary.
5. **Visualization**: Generates a word cloud to visualize the most frequent words in the article.
6. **User Interface**: Provides a web interface using Gradio for users to input text and receive a summary.

## Detailed Explanation

### 1. Environment Setup

The notebook begins by installing and importing necessary libraries such as `streamlit`, `pandas`, `wordcloud`, `nltk`, `networkx`, and `gradio`. These libraries are essential for data manipulation, visualization, and building the user interface.

### 2. Data Loading

The project reads a CSV file (`articles1.csv`) containing articles into a Pandas DataFrame. This data serves as the input for the summarization process.

### 3. Text Preprocessing

The preprocessing step involves several tasks:
- **Lowercasing**: Converts all text to lowercase.
- **HTML Cleaning**: Removes HTML tags from the text.
- **Email and URL Removal**: Strips out email addresses and URLs.
- **Contraction Expansion**: Expands contractions (e.g., "don't" to "do not").
- **Punctuation Removal**: Eliminates punctuation from the text.
- **Stopword Removal**: Removes common stopwords using NLTK's stopword list.

### 4. TextRank Algorithm

The TextRank algorithm is implemented to rank sentences based on their importance:
- **Sentence Tokenization**: Splits the article into sentences.
- **Graph Construction**: Constructs a graph where sentences are nodes, and edges represent similarity between sentences.
- **PageRank Calculation**: Uses NetworkX to calculate PageRank scores for each sentence.
- **Summary Generation**: Selects the top-ranked sentences to form the summary.

### 5. Visualization

A word cloud is generated using the `wordcloud` library to visualize the most frequent words in the article. This provides an intuitive representation of the text's content.

### 6. User Interface

The project uses Gradio to create a simple web interface:
- **Input**: Users can input an article in a text box.
- **Output**: The summarized text is displayed in another text box.
- **Launch**: The interface is launched locally, allowing users to interact with the summarization tool.

## How to Run

1. **Install Dependencies**: Ensure all required packages are installed. You can use the `!pip install` commands provided in the notebook.
2. **Run the Notebook**: Open `main.ipynb` in Jupyter Notebook or Jupyter Lab and execute the cells sequentially.
3. **Use the Interface**: Once the Gradio interface is launched, input your text to receive a summary.

## Conclusion

This project demonstrates the application of the TextRank algorithm for text summarization, providing a practical tool for condensing large articles into concise summaries. The integration of visualization and a user-friendly interface enhances the usability and accessibility of the tool. 