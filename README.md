# Mental Health Classification </br>
## About </br>
Twitter is currently one of the most influential social media. So many individuals take advantage of this social media to express feelings, opinions and suggestions to the public space. The issue of mental health is one of the issues that is often discussed and is currently hot in the general public on social media. The data used comes from collecting data directly on the Twitter platform, especially in Indonesia. A total of 5,000 data were taken for the labelling process manually by considering the same label naming by 2 researchers. Data labelling is divided into 8 classes, namely Awareness, Feelings and Problematization, Classification, Accessibility and Funding, Stigma, Service, Youth and Others. A total of 3,828 data were obtained through this process which were further divided into 2 categories. The first category contains 2 classes, namely Others and Non-Others. While the second category contains 7 classes, namely Awareness, Feelings and Problematization, Classification, Accessibility and Funding, Stigma, Service, and Youth. The best results in both categories use the BERT model with the pretrained model 'indolem/indobertweet-base-uncased'. In the first category get an accuracy of 80%. While in the second category get an accuracy value of 70%</br>
## Algorithm
- Bag of Words (BoW)</br>
- TF-IDF </br>
- N-Grams</br>
- Fasttext (Using pretrained ID)</br>
- BPE (Using pretrained ID)</br>
- GloVe (Using pretrained Twitter Multilingual)</br>
- BERT</br>
## Pretrained Model 
- Fasttext
  Pretained available here : https://fasttext.cc/docs/en/crawl-vectors.html </br>
  This paper using Indonesian Word Vector (300 Dimension)</br>
- BPE (Byte Pair Encoding)
  Pretrained available here : https://bpemb.h-its.org</br>
  This paper using Indonesian Embedding (100.000 Vocab Size & 100 Dimension)</br>
- GloVe
  Pretrained available here : https://nlp.stanford.edu/projects/glove/ </br>
  This paper using Twitter Word Vector (200 Dimension) </br>
  For Information, GloVe was training on large dataset containing multi-language</br>
## BERT
- indolem/indobertweet-base-uncased</br>
- indolem/indobert-base-uncased</br>
- bert-base-multilingual-uncased</br>
- Twitter/twhin-bert-base</br>
All BERT pretained model available on huggingface. You can try with different pretrained model
## Setup
All model above was trained on M1 GPU using Tensorflow and PyTorch (BERT). 3 models that is Fasttext, BPE and GloVe using bidirectional LSTM architecture.</br>
## 2 Stage Classification
### 2-Class (Filtering)
For non-contextual model using 'adam' optimizer, lr 1e-3 and 10 epoch. BERT using 'adamw' optimizer, lr 9e-5 and 3 epoch.</br>
| Model | Macro Avg. | Precision Macro Avg. | Recall Macro Avg. | F1 Accuracy |
| :---: |:----------:|:--------------------:|:-----------------:|:-----------:|
| BoW | 0.47 | 0.53 | 0.49 | 0.5 |




### 7-Class 
For non-contextual model using 'adam' optimizer, lr 1e-3 and 30 epoch. BERT using 'adamw' optimizer, lr 5e-5 and 3 epoch.</br>
## Our Paper
Stay Tune :D

  
