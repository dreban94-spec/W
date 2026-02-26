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
