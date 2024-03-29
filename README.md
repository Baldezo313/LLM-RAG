# LLM-RAG
Retrieval Augmented Generation (RAG) seems to be quite popular these days. Along the wave of Large Language Models (LLM’s), it is one of the popular techniques to get LLM’s to perform better on specific tasks such as question answering on in-house documents

## RAG Overview  
RAG has two main parts, retrieval and generation. In the first part, retrieval is used to fetch (chunks of) documents related to the query of interest. Generation uses those fetched chunks as added input, called context, to the answer generation model in the second part. This added context is intended to give the generator more up-to-date, hopefully better, information to base its generated answer on than just its base training data.  

## Building the RAG Input, or Chunking Text  
LLM’s have a maximum context or sequence window length they can handle, and the generated input context for RAG needs to be short enough to fit into this sequence window. We want to fit as much relevant information into this context as possible, so getting the best “chunks” of text from the potential input documents is important. These chunks should optimally be the most relevant ones for generating the correct answer to the question posed to the RAG system.
