## **Project Title**: Building a Simple Information Retrieval System using BM25 and GPT-3 and evaluated in the CISI collection.


**Project Overview**

The aim of this project is to introduce students to the basics of Information Retrieval (IR) and the BM25 ranking algorithm. The sollution to this project will help us to select the students to attend the course on deep learning applied to search. The students will build a simple IR system that retrieves relevant documents from a pre-defined corpus based on the user's query. The students will also use the chatGPT to assist in all phases of the project. The coding will be done using Google Colab notebooks and the deliverables will be placed in github account.

**Construction**

I started the project by asking ChatGPT how to build a simple information retrieval system using the BM25 algorithm in CISI collection. The ChatGPT answered the following steps:

* **Prepare the Data:** Download the CISI collection, which contains a set of documents, queries, and relevance judgments. The collection is available in different formats, such as plain text or XML. You need to parse the data and create an index for the documents.
* **Tokenize and Normalize the Text:** Before creating an index, you need to preprocess the text by tokenizing and normalizing it. Tokenization involves splitting the text into individual terms or tokens, while normalization involves converting the tokens to a canonical form. For example, you can convert all tokens to lowercase, remove stop words, and apply stemming or lemmatization to reduce inflectional forms to their base form.
* **Create an Inverted Index:** An inverted index is a data structure that maps each term to a list of documents that contain that term. The inverted index is the core data structure used in Information Retrieval systems. You can create an inverted index by iterating over the documents, tokenizing and normalizing the text, and updating the index with the term-document pairs.
* **Compute the IDF Weights:** IDF stands for Inverse Document Frequency, which measures the rarity of a term in the collection. You can compute the IDF weight for each term by dividing the total number of documents by the number of documents that contain the term and taking the logarithm of the result.
* **Rank the Documents:** To rank the documents for a query, you can use the BM25 ranking function, which is a variant of the TF-IDF weighting scheme. BM25 takes into account the term frequency, document length, and document frequency of each term in the query and the document. You can implement the BM25 ranking function by iterating over the query terms and the document terms and computing the score for each document.
* **Evaluate the System:** To evaluate the performance of the Information Retrieval system, you can use the relevance judgments in the CISI collection. You can compare the top-ranked documents for each query with the relevant documents and compute metrics such as precision, recall, and F1-score.

After reading the instructions, I asked ChatGPT to write the code in Python.
He wrote the code, but there are some problems with the implementation, as described below:
* The function that loads the texts in the CISI dataset has a problem with the parser, and the list with tokens was empty.
* The function that evaluates the system searches for some ids that exist in the queries array and doesn't exist in the evaluation array.
* The code doesn't generate a function to read and process the data.


**TODO**
Wrote about MRR10