# Vector-Space-Model
Vector Space Model (VSM) Document Ranking System
Overview
This project implements a Vector Space Model (VSM)-based document ranking system designed to retrieve and rank text documents based on their relevance to user queries. The system processes a collection of text files, calculates term frequencies (TF), inverse document frequencies (IDF), and TF-IDF weights, and uses cosine similarity to rank documents. A graphical user interface (GUI) built with Python's tkinter package allows users to input queries and view ranked results interactively.

The project was developed by Dilawer Khan (CS_06) and Bilal Hassan (CS_37) as part of an academic effort to explore information retrieval techniques.

Features
Document Retrieval: Reads and processes .txt files from a specified directory.
Preprocessing: Normalizes text by removing punctuation and converting to lowercase.
Vocabulary Creation: Builds a unique word list from the document collection.
TF-IDF Calculation: Computes term frequencies, document frequencies, and inverse document frequencies to assign weights to terms.
Query Processing: Accepts user queries and converts them into vector representations.
Cosine Similarity: Ranks documents based on their similarity to the query.
GUI: Provides an intuitive interface for query input and result display, including clickable document links to view content.
Objectives
Build an efficient document evaluation system using the Vector Space Model.
Reduce the time and effort required to find relevant documents.
Deliver precise and meaningful search results through TF-IDF and cosine similarity.
Enable users to explore ranked documents via a user-friendly GUI.
Prerequisites
Python 3.x: Ensure Python is installed on your system.
Required Libraries:
os: For file and directory operations.
tkinter: For the graphical user interface.
scrolledtext (from tkinter): For displaying scrollable text in the GUI.
math: For logarithmic calculations in IDF computation.
To install dependencies (if not already available):

pip install tk

Installation
Clone or Download: Obtain the project files from the repository or source.
Set Directory: Place your .txt document collection in the directory specified in the code (default: "D:\Aoa Project final"), or update the directory variable in Main_Function() to point to your document folder.
Run the Program: Execute the Python script to launch the GUI:

python vsm_document_ranking.py

Usage
Launch the application by running the script.
Enter a query in the provided text box in the GUI.
Click the "Search Document" button to process the query.
View the ranked list of documents with their cosine similarity scores.
Click on a document name (in blue) to display its content in a new window.

Algorithm Details
The system follows these steps:

Read Document Files: Loads text files from the specified directory into a dictionary.
Preprocess Documents: Removes punctuation and standardizes text.
Create Vocabulary: Extracts and sorts unique words from all documents.
Calculate Term Frequencies (TF): Counts word occurrences in each document.
Calculate Document Frequencies (DF): Determines how many documents contain each word.
Calculate Inverse Document Frequencies (IDF): Applies a logarithmic formula to emphasize rare terms.
Calculate TF-IDF Weights: Combines TF and IDF for each term-document pair.
Process User Query: Converts the query into a vector using the vocabulary.
Calculate Cosine Similarity: Measures similarity between the query vector and document vectors.
Rank Documents: Sorts documents by similarity scores in descending order.
Display Results: Shows ranked documents in the GUI.

Time Complexity

Total: O(n * m) + O(n * log(n)) + O(k)
n: Number of documents
m: Number of unique words in the vocabulary
k: Average document or query length

Space Complexity

Total: O(n * k) + O(m) + O(n * m) + O(n)

Limitations

Assumes the document collection is representative of the domain.
Preprocessing (e.g., stop word removal) may remove important keywords, impacting accuracy.
Treats words as independent features, ignoring context and semantic relationships.

Experimental Setup

Language: Python
Libraries: os, tkinter, scrolledtext, math
GUI Components: Text widgets, buttons, labels, and input fields for interactivity.
Results
Initial output: A query input box.
After query submission: A ranked list of documents with similarity scores.
Document content viewable by clicking on ranked document names.
Code Structure
Main_Function(): Core logic for reading files, processing queries, and ranking documents.
cosine_similarity(): Calculates similarity between query and document vectors.
Supporting functions: Handle GUI creation, file reading, and result display.
References
OpenAI: https://openai.com
License
This project is intended for educational purposes.
