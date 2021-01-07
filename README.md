#Email_reply_prediciton

## Table of contents
* [Problem Statement](#Problem Statement)
* [Dataset](#Dataset)
* [Approach](#Approach)
* [Results](#Results)
* [Future Work](#Future Work)
* [Contact](#contact)

## Problem Statement 
To predict: Reply/ No reply 

## Dataset
[Enron Email Dataset](https://www.cs.cmu.edu/~enron/): This dataset was collected and prepared by the CALO Project (A Cognitive Assistant that Learns and Organizes). It contains data from about 150 users, mostly senior management of Enron, organized into folders. The corpus contains a total of about 0.5M messages. This data was originally made public, and posted to the web, by the Federal Energy Regulatory Commission during its investigation.


## Approach
<ol>
  <li>Load Data </li>
  <li>Extracting Data: Extracting text email subject and body data from the text file</li>
  <li>Data Cleaning and Preprocessing </li>
  <li>Feature engineering : extracting additional features from emails (such as header subject length, email body lengths, recepient count, attachment count)</li>
  <li>Modelling:</li>
  <ol>
    <li>BERT Embeddings from the text data</li>
    <li>combine with other features</li>
    <li>train test split</li>
    <li>predict using MLP classifier</li>
    <li>check F-1 score and plot ROC</li>
  </ol>
</ol>

## Results
Scores I get is:<br>
   Model                                                       |   F1         |  AUC      |   
   ------------------------------------------------------------|--------------|-----------|
   Bert Embeddings + Original features + 2 engineered features |   0.88       |   0.91    |
   BERT Embeddings + Original feature + 4 engineered features  |   0.90       |   0.91    |   

## Future Work 
Generating embedding from
   * TF_IDF<br>
   * Word2Vec<br>
   * Doc2Vec<br>
and  training them with LSTM 

## Contact
Created by [@Anurag Sharma](https://www.linkedin.com/in/anurag-sharma-0308/) - feel free to contact me!
