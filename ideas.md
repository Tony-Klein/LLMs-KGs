Sources that inspired this document:
- [freeCodeCamp.org - Learn RAG From Scratch – Python AI Tutorial from a LangChain Engineer](https://youtu.be/sVcwVQRHIc8?si=d-cAX2okDj5bJmfb)
  - [GitHub - langchain-ai / rag-from-scratch](https://github.com/langchain-ai/rag-from-scratch)
  - [https://www.freecodecamp.org/news/mastering-rag-from-scratch/](https://www.freecodecamp.org/news/mastering-rag-from-scratch/)
- [freeCodeCamp.org - RAG Fundamentals and Advanced Techniques – Full Course
](https://youtu.be/ea2W8IogX80?si=lKfzFOJyoIc5y3sd)
- [AI Engineer - Architecting and Testing Controllable Agents: Lance Martin](https://youtu.be/ib-wTAvCZqg?si=-Eq9T0GSrzgQabuw)
- [LangChain - How to](https://python.langchain.com/docs/how_to/)


# RAG from Scratch
Definition of RAG:
> RAG combines external knowledge with LLMs for improved task performance, integrating domain-
specific information to ensure factuality and credibility. [Peng et al.](https://doi.org/10.48550/arXiv.2408.08921)

## Overview

[...]

- Basic:
  - Indexing
  - Retrieval
  - Generation
- Advanced:
  - Query transformations
  - Routing
  - Query construction
  - Indexing
  - Retrieval
  - Generation

Sources:
- [https://huggingface.co/blog/mixtral](https://huggingface.co/blog/mixtral)
- [https://x.com/RihardJarc/status/1778082161595208124](https://x.com/RihardJarc/status/1778082161595208124)
- [https://x.com/karpathy/status/1707437820045062561?s=20](https://x.com/karpathy/status/1707437820045062561?s=20)

## Basic Indexing

[...]

Sources:
- [https://python.langchain.com/docs/integrations/providers/](https://python.langchain.com/docs/integrations/providers/)
- [Greg Kamradt - ChunkViz v0.1](https://chunkviz.up.railway.app)
- [YouTube - Greg Kamradt - The 5 Levels Of Text Splitting For Retrieval](https://youtu.be/8OJC21T2SL4?si=lKSnKqFQfD9YP5EE)

## Basic Retrieval

- Split documents into smaller chunks, that can be easily embedded.
- Reasons:
  - LLM Context-Windows
  - the smalle the embedded chunks, the more precise vector embeddings

Sources:
- [https://simonwillison.net/2023/Oct/23/embeddings/](https://simonwillison.net/2023/Oct/23/embeddings/)
- [https://www.pinecone.io/learn/series/faiss/hnsw/](https://www.pinecone.io/learn/series/faiss/hnsw/)
- [https://python.langchain.com/docs/integrations/providers/](https://python.langchain.com/docs/integrations/providers/)
- [https://superlinked.com/vector-db-comparison](https://superlinked.com/vector-db-comparison)

  
## Basic Generation

Taking retrieved documents and stuffing them into the LLM Context Window.
 
Sources:
- [https://python.langchain.com/v0.1/docs/use_cases/question_answering/](https://python.langchain.com/v0.1/docs/use_cases/question_answering/)
- [https://python.langchain.com/docs/how_to/#qa-with-rag](https://python.langchain.com/docs/how_to/#qa-with-rag)
- [https://python.langchain.com/v0.1/docs/expression_language/](https://python.langchain.com/v0.1/docs/expression_language/)
- [https://python.langchain.com/docs/concepts/lcel/](https://python.langchain.com/docs/concepts/lcel/)

## Query Translation
### Multi-query

If the query is poorly written (because we are typically doing some kind of semntic similraity search betweet query and documents), we won't retrieve the proper documents.

Questions have a certain level of abstraction. Along this scale of abstraction a step-back question is a more abstract question, while a sub-question is a less abstract and more concrete question.

Problem:
The way a question was originally worded, might not be well aligned (or in close proximity in this high dimensional embedding space) to a document we want to retrieve.

Idea: By re-writing the question in different ways, we might be able to increase the lieklihood of actually retrieving the document that we actually want to retrieve.

Sources:
- [https://x.com/abacaj/status/1652011519863926786](https://x.com/abacaj/status/1652011519863926786)
- [LangChain - How to use the MultiQueryRetriever](https://python.langchain.com/docs/how_to/MultiQueryRetriever/)

  
### RAG Fusion
### Decomposition
### Step-back
### HyDe

## Routing
### Logical Routing
### Semantic Routing

## Query Construction
### Relational DBs (Text-to-SQL)
### GraphDBs (Text-to-Cypher)
### VectorDBs (Self-query retriever)

## Indexing
### Chunk Optimization
#### Semantic Splitter
### Multi-represantation Indexing
#### ParentDocument
#### Dense X
### Specialized Embeddings
#### Fine-tuning
#### Colbert
### Hierarchical Indexing
#### RAPTOR

## Retrieval
### Ranking
#### Re-Rank
#### RankGPT
#### RAG-Fusion
### Refinement
#### CRAG
### Active Retrieval
### CRAG
- [Corrective Retrieval Augmented Generation](https://doi.org/10.48550/arXiv.2401.15884)
- [LangChain - Building Corrective RAG from scratch with open-source, local LLMs](https://youtu.be/E2shqsYwxck?si=qg199MKQ84dtDe6U)


## Generation
### Active Retrieval
#### Self-RAG
- [Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection](https://doi.org/10.48550/arXiv.2310.11511)
#### RRR

# Other Stuff that needs to be organized

## Chunking
- Semantic Chunking
  - [YouTube - Greg Kamradt - The 5 Levels Of Text Splitting For Retrieval](https://youtu.be/8OJC21T2SL4?si=lKSnKqFQfD9YP5EE)
  - [LangChain - Semantic Chunking](https://python.langchain.com/v0.1/docs/modules/data_connection/document_transformers/semantic-chunker/)
  - [LangChain - AI21SemanticTextSplitter](https://python.langchain.com/v0.1/docs/integrations/document_transformers/ai21_semantic_text_splitter/)

## random
- Naive RAG (vectorbased)
- Advanced RAG
- GraphRAG
- Agents
- Knowledge Graphs
- Graph Neural Networks
- Self-RAG, Corrective RAG, + Adaptive RAG in LangGraph
