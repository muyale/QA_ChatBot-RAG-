# QA_ChatBot for Introverts
Introverts form the minority personality in the workforce and our individual communities. As an INTROVERTED individual it is often a good thing 
tochoose your career wisely.For most introverts ,career choices are forced upon them defeating the inherent satisfaction that comes
with having a job that you do not dread for the most part of your life. Job choices can be due to strengths and or weaknesses.
For an introvert a job that involves so much socialization isn't a good fit and so for careers in the sales and department,introverts 
can really struggle. Susan Cain has tons of career advice from her time as a corporate lawyer to being a writer ,she also has done 
a research on this problem and published it in her book : Quiet(The Power of Introverts in a world that can't stop talking) 

# About Problem : Career Guidance 
There is need for career guidance and so we can use Artificial Intelligence ,to come up with suggestions on best careers and practices
in the introverts worklife. 






# Objective

Use Falcon LLM, Langchain and ChromaDB to create a Retrieval Augmented Generation (RAG) system. This will allow us to ask questions about our documents (that were not included in the training data), without fine-tunning the Large Language Model (LLM). When using RAG, if you are given a question, you first do a retrieval step to fetch any relevant documents from a special database, a vector database where these documents were indexed.

![image](https://github.com/muyale/QA_ChatBot-RAG-/assets/111242297/7d67e45e-42a8-4863-b233-17eb0426ada2)





![image](https://github.com/muyale/QA_ChatBot-RAG-/assets/111242297/5c4d35fa-b66e-4165-8748-d0f28de4dd5f)





![image](https://github.com/muyale/QA_ChatBot-RAG-/assets/111242297/29183f00-edec-4cd5-9105-20021dd1df03)




# Definitions

LLM - Large Language Model
Falcon LLM
Langchain - a framework designed to simplify the creation of applications using LLMs
Vector database - a database that organizes data through high-dimmensional vectors
ChromaDB - vector database
RAG - Retrieval Augmented Generation (see below more details about RAGs)
Model details
Model: falcon 7b instruct
Variation: 7b-chat-hf(hugging face)
Version: V1
Framework: PyTorch
falcon model is pretrained and fine-tuned with 2 Trillion tokens and 7 to 70 Billion parameters which makes it one of the powerful open source models. It is a highly improvement over LlaMA 1 model.

#  What is a Retrieval Augmented Generation (RAG) system?

Large Language Models (LLMs) has proven their ability to understand context and provide accurate answers to various NLP tasks,
 including summarization, Q&A, when prompted. 
While being able to provide very good answers to questions about information that they were trained with, they tend to hallucinate when the topic is about information that they do "not know", i.e. was not included in their training data.
 Retrieval Augmented Generation combines external resources with LLMs. The main two components of a RAG are therefore a retriever and a generator.

The retriever part can be described as a system that is able to encode our data so that can be easily retrieved the relevant parts of it upon queriying it. The encoding is done using text embeddings, i.e. a model trained to create a vector representation of the information. The best option for implementing a retriever is a vector database. As vector database, there are multiple options, both open source or commercial products. Few examples are ChromaDB, Mevius, FAISS, Pinecone, Weaviate. Our option in this Notebook will be a local instance of ChromaDB (persistent).

For the generator part, the obvious option is a LLM. In this I used falcon  large language model

The orchestration of the retriever and generator will be done using Langchain. A specialized function from Langchain allows us to create the receiver-generator in one line of code.

#  Retreival Argument Generation

![image](https://github.com/muyale/QA_ChatBot-RAG-/assets/111242297/e5459c28-79a0-4d1b-9b6d-6fa0da885df7)


The main objective of this project was to create an AI ChatBot that give sound career advice based on Susan Cain's book quiet .
The method of operation was to train the LLM(falcon ) on data (Susan cains'text) using RAG and then use the information learnt by 
the LLM to generate appropriate responses.


  
Future Developments 
Creating a UI 
Using Reasoning Skills by AI
Training the ChatBot on multiple perspectives .
