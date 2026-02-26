# W
W
Title name:

Public Services Appointment Scheduling Assistant

Problem Statement:

Citizens often face difficulties scheduling appointments for public services due to complex procedures and limited information availability.

Steps:

Develop an Al agent that guides users through appointment scheduling processes.

Use Langchain or Liamaindex to interpret scheduling rules and available slots.

Enable the agent to answer questions and book appointments based on user input.

Demonstrate with sample scheduling data.

Data Requirements:

Appointment schedules, service availability, procedural guidelines. Sample data can be created or sourced from public service portals.

Expected Output:

Interactive text-based appointment booking confirmations and guidance.


   code for service embedded:----
  fron Sangchain.text splitter import RecursiveCharacterTextSplitter

fron Langchein opanai impart ChatOpenAI, OpenATEnbeddings

fron langchain community.vectorstores Leport Chroma

fron langchain.chains irport. RetrievalQA

import os

import http

from wngchain.document loaders import CSVLoader

as.ewiren["KMP DUPLICATE LIB_OK" - "TRUE"

tiktoken cache_dir"./tiktoken_cache"

[[

client https.Client(verify-False)

LLM and Enbedding setup

1inchatOpenAT

base url="https://matlab.tcs.in",

models"asure L/genallab-maas-DeepSeek-V3-8324",

aod kaysk-PeZT4C3140FOPQ

httpclienteclient

mbedding model Opansbeding

bowe url-https://gonalisb.tcs in 


code for the 2 pic 
wwhadding model = OpenAlEmbeddings(

public service appointmes.ca

toan cache

27

agarnby

spp. py

base_url="https://ganailab.tes.in",

agent.py

models"asure/gunsileb-maas-text-embedding-3-large",

api key="sk-PmZ31414rtCh310FOPQ",

http clientwclient

def Service(proaptistr):

Step 1: Loed CSV using LangChain's CSVLoadar

Loader CSVLoader(fils paths Dataset/public_service appointments. την")

This returns Ilat of Document abjects

documents Loader.load()

Step 2: Chunk the documents

test splitter RecursiveCharacterTextl@litter(chunk kim100e, chunk overlap-100) chunks text splitter.split_documente (documents) Split hased on t

vectordb Chrome, Froe documents(chunks, erbedding model, persist directorye",/chrome indes")

vectordb.persist()

tad Chain

retriever vectordo.as renteven(search type "similarity", search harga (k": 3))


code for the third pic. Step 2: Chunk the documents content

40

41

42

43

44

54

55

text splitter RecursiveCharacterTextSplitter(chunk_size=1000, chunk_overlap-280) chunks taxt splitter.split_documents (documents) # Split based on Documents

vectordb Chroma.from documents (chunks, embedding model, persist_directory="./chroma_index")

vectordb.persist()

Step 4: RAG Chain

retriever veetordb.as_retriever(search_type="similarity", search kwargs={"k": 3))

rag chain RetrievalQA.from_chain_type(

11m-11m,

retriever-retriever,

return_source_documents True

#Step 5: Ask summarization prompt

#summary prompt "find the best hotel location in mumbai with rating 4 star and above with di

#result rag _chain.run(summary prompt)

result rag chain. Invoke("Show slots for Aadhaar booking in morning shift")

print(result)

return result
