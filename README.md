# Sytematic-Evalution-of-Document-Embedding-Techniques

This work systematically evaluates document embedding techniques, including models such as TF-IDF, LDA, Doc2Vec, BERT, and Llama 3. The evaluation involves generating embeddings based on three datasets and assessing their performance. These datasets consist of news articles along with their associated categories. 

The evaluation process involves forming clusters and assessing them using metrics like Homogeneity, Completeness, V-measure, and Adjusted Rand Index. These metrics provide insights into how well the embeddings capture data structures and group similar content. Additionally, the average cosine similarity within and between categories is examined. This measure indicates how similar documents are and how closely they are placed in the vector space. These two types of metrics are used for the evaluation.

The evaluation of the various models was conducted using Google Colab.

# Conditions for Generating Embeddings

Since the generation of embeddings was executed in Google Colab, the datasets were specified as paths within the models. The files are stored on this GitHub repository, so placing the Implementation folder in MyDrive should ensure everything works optimally. However, if the path is changed, it must be adjusted for each dataset accordingly. 

Furthermore, BERT requires at least a T4 GPU and Llama 3 requires an A100 GPU in Google Colab.

Additionally, a token from Hugging Face is required to work with Llama 3. This token needs to be entered when prompted.

It is recommended to run each section sequentially in Google Colab to avoid complications between different datasets. The easiest way to do this is by clicking on "Runtime" and then "Run All." For each file, access to MyDrive must be granted. Additionally, for the Llama models in the "Load Model" section, you will need to enter the token.

# General Procedure
The overall procedure in the Google Colab files is the same for each model. It consists of two main parts: the Preprocessing Steps and the Embedding Step. The Embedding Step includes the generation of embeddings, clustering, and evaluation.

## Preprocessing Steps
Each model follows the same set of steps. First, preprocessing steps are executed, which involve importing and installing various libraries. Additionally, this step prepares the dataset to ensure the model can effectively work with the data. For the transformer models, the pretrained model is also loaded during this step.

## Embedding on Dataset

In this section, embeddings are generated for the dataset using various models. Each model processes the dataset to create vector representations that capture the semantic structure of the documents. 

These embeddings will be used for clustering and evaluating the performance of each model. 

This process is identical for each dataset. For Doc2Vec the architectures Distributed Memory and Distributed Bag of Words are utilized. In the case of BERT, different layers are tested on the first dataset to evaluate the transformer architecture.

# Step-by-Step Guidance:

1. **Manage File Paths**:
   - The datasets are specified as paths within the models. Place the **Implementation** folder in your MyDrive to ensure everything functions properly. If you change the path, make sure to adjust it for each dataset accordingly.
   
2. **Set Up Google Colab**:
   - Ensure that you run each section of the notebook sequentially to prevent complications across different datasets. The simplest method is to click on **"Runtime"** and then select **"Run All."**
  
3. **Token Requirement**:
   - When working with Llama 3, a token from Hugging Face is necessary. Be prepared to enter this token when prompted during the model loading process.

4. **Access MyDrive**:
   - For each file, you will need to grant access to your Google Drive. This is essential for reading the datasets and storing results.


# Conclusion

To systematically evaluate document embedding techniques, follow these steps to ensure a smooth execution of the process using Google Colab. This workflow involves various models, including TF-IDF, LDA, Doc2Vec, BERT, and Llama 3, applied to three datasets consisting of news articles and their associated categories.

# Dataset
* https://www.kaggle.com/datasets/rafsunahmad/classify-news-into-category
* https://www.kaggle.com/datasets/setseries/news-category-dataset
* https://www.kaggle.com/datasets/kotartemiy/topic-labeled-news-dataset
