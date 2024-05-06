#  Article Retrieval in response to queries

## Overview

Article Retrieval is a notebook implementing Retrieval Augmented Generation. It uses the following 
[Kaggle dataset](https://www.kaggle.com/datasets/meruvulikith/1300-towards-datascience-medium-articles-dataset) to enhance its responses to queries.

The system uses a Chroma database for similarity search among the articles and a **Mistral 7B** model for cohesive answer generation based on the articles found.

## Usage

The models are quite computationally heavy and need a GPU with at least 16GB of RAM. Running the code on an external GPU such as Kaggle is advised.

The system can be set up by running all the cells in the notebook. The paths of the dataset and models are set up to be run on the Kaggle website. The necessary installations are included in the code. 

At the end of the notebook, a sample query is provided. 

### Query Answering
The main goal of the program is to answer queries related to the topics in the imported dataset based on its articles. This can be done by the code below.
``` python
answer_query("Your question")
```

### Article Retrieval
The program also allows for the sole retrieval of articles answering or related to the question given. This is done by the following command, replacing "k" with the number of relevant articles the user wants to see.
```python
print(retrieve_articles("Your question", k))
```
