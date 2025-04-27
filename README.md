# Decoding the Divine: Religious Affiliation Prediction using Multiple Model Approaches
DSAN6600 Project Group #4\
Sophia Rutman, Courtney Green, Lizzie Healy, Caroline Delva

## Purpose
The purpose of this project was to test three machine learning algorithms on their ability to classify relgious affliation groups. The models were each trained and tested on a survey conducted by the Pew Research Center entitled _Religious Landscape Study_, which aimed to understand the state of religion across the United States. 

We set out to achieve two goals: 
  1. **Predict religious affiliation**: Determine if religion can be predicted based on personal demographics, religious practices, social values, and political goals (ie. are there palpable comminalities between individuals belonging to the same religious group).
  2. **Evaluate machine learning tools**: Gain a better sense of the current state of machine learning tools and uncover which is best applied to multi-classification tasks.

## Set-up Instructions 
While this work is mainly done for the purposes of creating a report and not code sharing, it is nonetheless, possible to re-utilize this work. To do so:
  1. Clone this repository to your local machine
  2. Install the required packages
  3. Download the Pew Research Center dataset (https://www.pewresearch.org/dataset/2023-24-religious-landscape-study-rls-dataset/)
  4. Run the main machine learning algorithm scripts located in the code folder
     a. python "code/clustering.qmd"\
     b. python "code/QDA.qmd"\
     c. python "code/MLP.ipynb"\
     d. python "code/transformer_13_classes.qmd"
  5. View the output produced or utilized the trained models for further usage.
It is also possible to view the output of these files without running them within the docs/code folder where you will find rendered versions of each of the workflows. 

## Usage Examples
While our project was primarily an academic and personal exploration of knowledge, the techniques and models could have broader applications:
  1. Targeted Religious Recruitment: Personalize outreach to relgiously affiliated individuals or identify those that may be good candidates for joining a specific religion.
  2. Political Polling: Refine political surveying strategies or predict political leanings based on religious groupings of the current US.
  3. Sociological Research: Get a better academic understanding of religious shifting overtime.
  4. Marketing Strategies: Understand how to advertise to specific relgious groups based on their beliefs and practices.

## Project Structure
/code/: code files for clustering, QDA, MLP, and transformer models\
/docs/: rendered version of the code files\
/docs/code/: clustering, QDA, MLP, transformer rendered output\
/README: project overview

## Abstract 
This study compared three machine learning algorithms for classifying religious groups using Pew Research Center survey data. Clustering analysis revealed meaningful overlap within traditions, especially among Protestants and the Religiously Unaffiliated, highlighting the complexity of religious labels and the challenges of perfect classification. The multi-layer perceptron achieved moderate performance (validation accuracy = 67.7%, precision = 65.2%, recall = 46.1%, F1 = 48.8%; test accuracy = 68.0%, macro F1 = 0.44, weighted F1 = 0.66), performing well on dominant classes but struggling with minority groups. Quadratic discriminant analysis reached 67% accuracy (weighted F1 = 0.70) for the full 13-class task and 89% (weighted F1 = 0.90) for a simplified version, though it failed to predict smaller groups (F1 = 0.00). The transformer, tuned through hyperparameter optimization, achieved the strongest results with a 94.9% test accuracy (macro F1 = 0.56, weighted F1 = 0.93). While it still struggled with minority classes, its self-attention mechanisms and learned embeddings enabled strong generalization across religious categories. Overall, these findings show that while machine learning models, especially transformers, can predict broad patterns of religious affiliation with impressive accuracy, capturing the full diversity and complexity of belief systems will require richer data, better modeling strategies, and improvements in survey design.
