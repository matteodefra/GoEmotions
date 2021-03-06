# GoEmotions
Sentiment analysis over GoEmotions dataset. 
<!--- In collaboration with [@orientino](https://github.com/orientino) and [@Gerlando30](https://github.com/Gerlando30). -->

## Description

We performed sentiment analysis over the [GoEmotions](https://arxiv.org/abs/2005.00547) dataset.

The objective of our work was to replicate the baseline model BERT experimented in the aforementioned paper, and then extend the analysis to multiple models derived from the same BERT.

In particular, we tested the following models:
- BERT
- BigBird
- DistilBERT
- RoBERTa

## Repository

๐GoEmotions                                 
โโ ๐analysis                                
โ  โโ ๐analysis_ekman.ipynb                 
โ  โโ ๐analysis_group.ipynb                 
โ  โโ ๐analysis_original.ipynb              
โโ ๐config                                  
โ  โโ ๐ekman.json                           
โ  โโ ๐group.json                           
โ  โโ ๐original.json                        
โโ ๐data                                    
โ  โโ ๐ekman                                
โ  โ  โโ ๐dev.tsv                           
โ  โ  โโ ๐labels.txt                        
โ  โ  โโ ๐test.tsv                          
โ  โ  โโ ๐train.tsv                         
โ  โโ ๐group                                
โ  โ  โโ ๐dev.tsv                           
โ  โ  โโ ๐labels.txt                        
โ  โ  โโ ๐test.tsv                          
โ  โ  โโ ๐train.tsv                         
โ  โโ ๐original                             
โ     โโ ๐dev.tsv                           
โ     โโ ๐labels.txt                        
โ     โโ ๐test.tsv                          
โ     โโ ๐train.tsv                         
โโ ๐src                                     
โ  โโ ๐bert_goemotions_pytorch.ipynb        
โ  โโ ๐bigbird_goemotions_pytorch.ipynb     
โ  โโ ๐distilbert_goemotions_pytorch.ipynb  
โ  โโ ๐roberta_goemotions_pytorch.ipynb     
โโ ๐README.md                               
  
The structure of the repository is showed above. In the _src/_ folder you can find the different notebook used for the experiments. If you want to replicate them, we suggest to change the baseline path directory based on you current file path accordingly.

We included also the different data and config files used to perform the experiment, plus the post analysis in the _analysis/_ folder.


## Results

We were able to reach the result of the original paper with an accuracy of around __0.45__ for the baseline BERT.
We discovered also that using a lightweight model as DistilBERT or a complex one like RoBERTa, slightly improve the results with respect to classical BERT.

Below we report the mean accuracy and standard deviation obtained over runs with different starting seeds for the tested models on the original taxonomy

![test_accuracy_original](images/test_accuracy.png "Test accuracy original")


## Contributors

[Matteo De Francesco](https://matteodefra.github.io/)

[Gerlando Gramaglia](https://github.com/Gerlando30)

[Chenxiang Zhang](https://github.com/orientino)
