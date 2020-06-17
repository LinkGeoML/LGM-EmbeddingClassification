# LGM-EmbeddingClassification
This repository contains the experimental code for learning FastText embeddings for representing POIs. These representations are then exploited in the POI categorization problem, formalized as a multiclass classification task.

## Dataset
The code utilizes the Yelp dataset, which can be downloaded [here](https://www.yelp.com/dataset). From the files available there, only the file 'business.json' is used, as it contains the necessary attributes about each Yelp business.

## Usage
For the execution of the code, the Yelp file 'business.json' needs to be downloaded first. It is suggested to create a 'data' folder to store this file and a 'ft_models' folder to store the trained FastText models for reusage. After these steps, the notebooks can be used to perform the following scenarios:

- Notebook '1-dataset_setup.ipynb' is used to load the dataset file and process it to come up with well organized train and test data subsets
- Notebook '2-baseline.ipynb' implements a baseline scenario using traditional td-idf features, in order to provide a comparison basis for the rest of the methods
- Notebook '3-fasttext.ipynb' trains a FastText model from scratch based on the POI attributes sequences. Then these representations are used for the classification task
- Notebook '4-spatial.ipynb' extends the above POI representations by incorporating spatial information. Each POI embedding is extended with the averaged representations of its neighbors
- Notebook '5-fasttext-gru.ipynb' utilizes pretrained FastText vectors in order to create POI embeddings. The pretrained vectors can be downloaded from [here](https://www.kaggle.com/yekenot/fasttext-crawl-300d-2m)
