# Bsuir Assistant Data Module
A repository for launching up the data collecting module for [BSUIR RAG Assistant](https://github.com/semantic-hallucinations/bsuir-assistant)

## Setting up

To run the this module you need:

* A __.env__ file which contains the environment variables for the services. Refer to __.env.example__

* A set up Docker compose, working example of which is provided in this repository

## Running

You need Docker to run the module. After setting up is complete, you can run it by writing in terminal in the root folder:

```bash
docker compose up
``` 

## IMPORTANT

[The Embedder](https://github.com/semantic-hallucinations/bsuir-helper-embedder) service for data module actually has 2 working images, for CPU and for GPU:

### Image for CPU
```yaml
services:
  bsuir-helper-embedder:
    image: ghcr.io/semantic-hallucinations/bsuir-helper-embedder:latest
 ```

### Image for GPU
```yaml
services:
  bsuir-helper-embedder:
    image: ghcr.io/semantic-hallucinations/bsuir-helper-embedder:cuda
 ```

__(!!!) It is highly recommended using the GPU image for actually using the module with active parser. Please refer to Requirements section of this README for seeing the system requirements for images__ 


## Requirements

### Basic:

* Fast internet connection

* Docker-compose

* Natural intelligence

### With CPU-based embedder:

* At least 15-20GB free storage space

* At least 8GB RAM

### With GPU-based embedder:

* The NVIDIA GPU

* At least 30-40GB free storage space

* At least 8GB RAM

* At least 4GB Video Memory

__*Warning*__ : This requirements data was specified by actually testing the [BAAI/bge-m3](https://huggingface.co/BAAI/bge-m3) model. For more detailed information, please refer to the provided link for the model itself and for the [embedder repository](https://github.com/semantic-hallucinations/bsuir-helper-embedder)

## Sources
This repository uses or refers to following services:

* [Data Loader](https://github.com/semantic-hallucinations/bsuir-helper-data-loader) by [Veterrius](https://github.com/Veterrius?tab=repositories) 

    Please check it out if you want to actually know what's going on there instead of just ruuning everything through this repository

* [Embedder](https://github.com/semantic-hallucinations/bsuir-helper-embedder) by [Veterrius](https://github.com/Veterrius?tab=repositories)

* [Parser](https://github.com/semantic-hallucinations/bsuir-site-parser) by [Mediano4e](https://github.com/Mediano4e)

* [BSUIR RAG Assistant](https://github.com/semantic-hallucinations/bsuir-assistant) by [Semantic Hallucinations](https://github.com/semantic-hallucinations)

