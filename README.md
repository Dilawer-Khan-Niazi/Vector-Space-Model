**Vector Space Model (VSM) Document Ranking System**
**Overview**
The Vector Space Model (VSM) Document Ranking System is a Python-based application designed to retrieve and rank text documents based on their relevance to user queries. Utilizing the Vector Space Model, the system processes a collection of text files, calculates term frequencies (TF), inverse document frequencies (IDF), and TF-IDF weights, and employs cosine similarity to rank documents. A graphical user interface (GUI) built with Python's tkinter package enables users to input queries and view ranked results interactively.
This project was developed by Dilawer Khan and Bilal Hassan Khan as part of an academic exploration of information retrieval techniques.
**Features**

Document Retrieval: Reads and processes .txt files from a specified directory.
Text Preprocessing: Normalizes text by removing punctuation and converting to lowercase.
Vocabulary Creation: Generates a unique word list from the document collection.
TF-IDF Calculation: Computes term frequencies, document frequencies, and inverse document frequencies to assign term weights.
Query Processing: Converts user queries into vector representations for comparison.
Cosine Similarity: Ranks documents based on their similarity to the query.
GUI: Provides an intuitive interface for query input, result display, and clickable document links to view content.

**Objectives**

Develop an efficient document evaluation system using the Vector Space Model.
Minimize the time and effort required to locate relevant documents.
Deliver precise and meaningful search results through TF-IDF and cosine similarity.
Provide a user-friendly GUI for exploring ranked documents.

**Prerequisites**

Python 3.x: Ensure Python is installed on your system.
Required Libraries:
os: For file and directory operations.
tkinter: For the graphical user interface.
scrolledtext (from tkinter): For scrollable text display in the GUI.
math: For logarithmic calculations in IDF computation.



**To install dependencies (if not already available):**
pip install tk

Installation

Clone or Download: Obtain the project files from the repository or source.
Set Directory: Place your .txt document collection in the directory specified in the code (default: D:\Aoa Project final), or update the directory variable in Main_Function() to point to your document folder.
Run the Program: Execute the Python script to launch the GUI:python vsm_document_ranking.py



**Usage**
Launch the application by running the script.
Enter a query in the provided text box in the GUI.
Click the Search Document button to process the query.
View the ranked list of documents with their cosine similarity scores.
Click on a document name (displayed in blue) to view its content in a new window.

**Algorithm Details**
The system operates through the following steps:

Read Document Files: Loads text files from the specified directory into a dictionary.
Preprocess Documents: Removes punctuation and standardizes text to lowercase.
Create Vocabulary: Extracts and sorts unique words from all documents.
Calculate Term Frequencies (TF): Counts word occurrences in each document.
Calculate Document Frequencies (DF): Determines the number of documents containing each word.
Calculate Inverse Document Frequencies (IDF): Applies a logarithmic formula to emphasize rare terms.
Calculate TF-IDF Weights: Combines TF and IDF for each term-document pair.
Process User Query: Converts the query into a vector using the vocabulary.
Calculate Cosine Similarity: Measures similarity between the query vector and document vectors.
Rank Documents: Sorts documents by similarity scores in descending order.
Display Results: Presents ranked documents in the GUI.

**Complexity Analysis**

Time Complexity:
Total: O(n * m) + O(n * log(n)) + O(k)
n: Number of documents
m: Number of unique words in the vocabulary
k: Average document or query length


Space Complexity:
Total: O(n * k) + O(m) + O(n * m) + O(n)


**Limitations**

Assumes the document collection is representative of the domain.
Preprocessing (e.g., stop word removal) may eliminate important keywords, affecting accuracy.
Treats words as independent features, ignoring context and semantic relationships.

**Experimental Setup**

Language: Python
Libraries: os, tkinter, scrolledtext, math
GUI Components: Text widgets, buttons, labels, and input fields for interactivity.

**Results**

Initial Output: A query input box.
Post-Query Submission: A ranked list of documents with similarity scores.
Document Interaction: Clickable document names to view content in a new window.

**Code Structure**

Main_Function(): Core logic for reading files, processing queries, and ranking documents.
cosine_similarity(): Computes similarity between query and document vectors.
Supporting Functions: Manage GUI creation, file reading, and result display.


**License**
This project is intended for educational purposes.
