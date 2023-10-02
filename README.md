# Semantic-Search-Summarizer

## Task :

To create a model which can when given a user input produces a summary of the most relevant information from the huge data corpus fed to it.

## Dataset :
`sus.json` contains a dictionary of list of information (paragraphs) about various topics.

## Approach: 


1. Using Asymmetric Semantic Search (where the `query` size and `data_corpus` size is different), to find the similarity between given data and the query.

 **Semantic Search** - The idea behind semantic search is to embed all entries in your corpus, which can be sentences, paragraphs, or documents, into a vector space. At search time, the query is embedded into the same vector space and the closest embedding from your corpus is found.


 2. Model Used - `msmarco-distilbert-base-dot-prod-v3` which uses dot product to find the similarity.

 3. Encodings and storing them - **FAISS**: (Facebook AI Similarity Search) is a library that allows developers to quickly search for embeddings of multimedia documents that are similar to each other.

 4. Summarizer : Used the `Hugging Face Pipeline` for the summarization with its default model (sshleifer/distilbart-cnn-12-6). However dedicated summarizer can be implemented to increase the efficiency and time optimization

 5. Finally saving the output to a ".txt" file

A sample of the produced summary is also given.

Article for reference :

1. https://medium.com/mlearning-ai/semantic-search-with-s-bert-is-all-you-need-951bc710e160#:~:text=The%20idea%20behind%20semantic%20search,from%20your%20corpus%20is%20found.

2. https://medium.com/artificialis/t5-for-text-summarization-in-7-lines-of-code-b665c9e40771
