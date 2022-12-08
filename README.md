# Few-Shot-Learning-with-Topic-Modeling

Few Shot Learning With Topic Modeling on IRS Bulletin(US tax data)

This repository contains various implementations of Few-Shot Learning techniques combined with Topic Modeling to predict topics discussed in the IRS tax data. The repository is divided into multiple independent directories, each focusing on a specific approach or technique.

The goal of this research is to analyze the topics discussed over the past 20 years in the IRS Bullietin and provide a trend of the topics discussed. Furthermore, the Few-Shot Learning model will help find the topic related to a section or paragraph.

### Main Features

- **Topic Model Directory**: Utilizes the BERTopic model to find topics in the given dataset.
- **Zero Shot Learning Directory**: Implements Zero Shot Learning to predict topics.
- **Few Shot Learning I and II Directories**: Implements two different Few-Shot Learning approaches to predict topics.

### Project Overview

The project is divided into two main tasks:

1. **Task 1: Topic Modeling and Visualization**

   - Evaluating topic models and extracting the top 20 topics from the corpus using Topic Modeling.
   - Tagging the topics to the documents.
   - Visualizing the trend across years.

2. **Task 2: Few-Shot/Zero-Shot Learning Models**
   - Creating Few-Shot and Zero-Shot learning models to predict relevant topics for the inputted sentence or paragraph.

### Data and Methods

The project uses IRS Bulletins, which include bulletins published weekly for the past 20 years in unstructured PDF format. Find Data here: [IRS](https://www.irs.gov/irb).

For dynamic BERTopic modeling, following methods are used:

- Embedding Models: Sentence Transformers, Flair, TF-IDF
- Dimensionality Reduction: UMAP
- Topics Representation & Clustering: c-TF-IDF, HDBSCAN

For text classification using Meta learning(ZSL and FSL), following methods are used:

- N-way-K-Shot Learning: Zero-Shot Learning, One-Shot Learning, Few-Shot Learning

### Zero-Shot Learning

Zero-Shot Learning aims to classify unseen topics without any trained topics. The implementation involves learning a joint embedding space between seen and unseen labels. The Flair package is used for this purpose, with the following types of transformers:

- Name Entity Recognition
- Text Tagging
- Text Embedding
- Classification: TARSClassifier

### Few-Shot Learning

Few-Shot Learning aims to classify new data, given a few samples. The implementation involves learning to learn by itself. The following packages and repositories are used:

- Package: SetFitClassifier
- Package: Pytorch
- Repo: Latent Text Embedding with SBERT

### Installation Steps

1. Clone the repository:
   ```
   git clone https://github.com/anujshah3/Few-Shot-Learning-with-Topic-Modeling.git
   ```
2. Install Python and Jupyter Notebook.

3. Create a virtual environment for each directory individually. Each directory has its own `requirements.txt` file.
   ```
   python -m venv venv
   source venv/bin/activate  # For Linux/Mac
   venv\Scripts\activate  # For Windows
   pip install -r requirements.txt
   ```

### Usage

Each directory is independent of the others, and you can run the Jupyter Notebooks within each directory to explore the respective implementations. This repository can also be used to train different datasets to predict topics using Topic Modeling and Meta Learning as well.
