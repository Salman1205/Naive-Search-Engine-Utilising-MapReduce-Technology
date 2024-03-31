# Naive-Search-Engine-Utilising-MapReduce-Technology
# Search Engine on Jupyter

This repository contains the code for implementing a search engine using Jupyter Notebook along with Hadoop MapReduce. The `search_engine_on_jupyter.ipynb` file serves as the main notebook where all the preprocessing, vocabulary generation, indexing, and similarity calculations are performed. Additionally, the MapReduce framework is utilized for scalability in processing large datasets.

## Functionality

In `search_engine_on_jupyter.ipynb`, the following functionalities are implemented:

- Preprocessing:
  - Stopword removal
  - Punctuation removal
  - Lemmatization
  - Lowercasing of text

- Vocabulary Generation:
  - Creation of a vocabulary of unique words
  - Indexing of the vocabulary

- Calculation of Term Frequency (TF), Inverse Document Frequency (IDF), and TF-IDF scores

- Similarity Calculation:
  - Scalar product to find similar articles for the query entered by the user

The MapReduce framework is employed for distributed processing with the following tasks:

### Mapper1 & Reducer1:
- Preprocessing
- Vocabulary generation

### Mapper2 & Reducer2:
- Indexing
- Calculation of TF, IDF, and TF-IDF

### Mapper3 & Reducer3:
- Preprocessing
- Vocabulary generation
- Calculation of TF, IDF, and TF-IDF for the user-entered query text

### Mapper4 & Reducer4:
- Calculation of scalar product between the TF-IDF of user's query text and all documents
- Output the article IDs of the top 5 similar articles

## Usage

To use the search engine:

1. Open `search_engine_on_jupyter.ipynb` in a Jupyter Notebook environment.
2. Run each cell sequentially to preprocess the data, generate vocabulary, calculate TF-IDF, and perform similarity calculations.
3. Enter a query text when prompted.
4. The notebook will output the top 5 similar articles based on the query.

For Hadoop MapReduce tasks:

1. Ensure Hadoop is properly installed and configured.
2. Run the appropriate MapReduce jobs (`mapper1`, `reducer1`, `mapper2`, etc.) passing the required input files and parameters.
3. Follow the pipeline as described in the notebook to execute the search and similarity calculation tasks.

## Dependencies

- Python 3
- Jupyter Notebook
- Hadoop MapReduce
