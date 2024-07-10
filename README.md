# Azure Video Analytics Demo

## Introduction

In this demo, we will show you some video analytics use case with Azure AI.

## Design

- Prepare the video data.
- Extract frames from the video data at regular intervals and save them as image files.
- Upload the video data and image files.
- Build an AI Search index including:
  - Captions
  - Caption Embeddings
  - Image Embeddings
  - Image URLs
  - Video URLs
  - Frame metadata (e.g., timestamps)
- Generate captions from the image data using GPT-4.
- Import the data into the index.
- Execute a query to retrieve 10 related images.
- Generate new video metadata using GPT based on the captions and frame metadata, including:
  - Frame order
  - Timestamps
  - Actions (optional)
- Reassemble the images into a video based on the video metadata.

## Prerequisites

* An Azure subscription. If you don't have an Azure subscription, [create a free account](https://aka.ms/AMLFree) before you begin.
* Azure AI Search resource, resource can be created via Azure Portal. [Read here](hhttps://learn.microsoft.com/eu-es/azure/search/search-create-service-portal)
* Azure OpenAI Service resource and model, recource can be created via Azure Portal. Model can be deployed via Azure OpenAI Studio. [Read here](https://learn.microsoft.com/eu-es/azure/ai-services/openai/how-to/create-resource?pivots=web-portal)
* Azure AI Vision resource, resource can be created via Azure Portal as multi-service resource for Azure AI services. [Read here](https://learn.microsoft.com/en-us/azure/ai-services/multi-service-resource?tabs=linux&pivots=azportal)
* Azure Storage Account and blob container, these can be created via Azure Portal. [Read here](https://learn.microsoft.com/eu-es/azure/storage/blobs/blob-containers-portal)
* Once you have created above resources, you need to set `.env` and define the following variables. These variables can be found in Azure Portal and Azure OpenAI Studio.
  * `AZURE_OPENAI_ENDPOINT`
  * `AZURE_OPENAI_API_KEY`
  * `AZURE_OPENAI_DEPLOYMENT`
  * `AZURE_OPENAI_API_VERSION`
  * `AZURE_SEARCH_ENDPOINT`
  * `AZURE_SEARCH_ADMIN_KEY`
  * `AZURE_AI_VISION_ENDPOINT`
  * `AZURE_AI_VISION_API_KEY`
  * `BLOB_CONNECTION_STRING`
  * `BLOB_CONTAINER_NAME`