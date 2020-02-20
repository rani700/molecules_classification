# Task

Given dataset contains following columns   
<b>molecule_name</b> - this contains 102 class of molecule  
<b>conformation_name</b> - All of which are unique  
<b>f1 - f166</b> - These are the features of every molecule and its conformation  
<b>class</b> - this column contains 0 or 1 (1 for musk and 0 for non-musk)  
    
So the classification model can be made either to classify between musk or no_musk  or 102 categories of molecules.  

## Pre Processing 
  
I have used StandardScaler for scaling the input data.  
This is necessary because we don’t know on what scale and range of the features are in. StandardScaler makes our data such that its mean value of 0 and standard deviation of 1. So that it helps in efficiency training our neural network model.  

## Models 
I have trained two deep learning algorithms viz, **Deep Neural Network** and  **Convolutional Neural Network** for both **musk vs non-musk classification** and also **102 category of molecules classification**.   
  
All these models performed well. But as there are 102 categories of molecules containing musk and non musk molecules. I have applied **transfer learning** as first training 102 category molecules and used the same model and added 2 layers to train for musk vs non musk.   
By using transfer learning I achieved **100% accuracy** in musk vs non musk classification.  
  
Details of which are described below.
Link for the jupyter notebooks on github and colab along with the link for the model files of all the models are at the end of this document in the form of table.  
  
### Accuracy Table
  

| |musk vs non-musk | 102 class of molecules|
| ---------- |:----------|:----------:|
|Deep neural network|Accuracy - 0.99924242424|Accuracy - 0.971969696969|
|Convolutional neural network|Accuracy - 0.99848484848| Accuracy - 0.956818181818|
|Transfer learning|Accuracy - 1.0 or 100%| |



### Code and model files

| |musk vs non-musk|102 class of molecules|
| ------- |:------:|:-------:|
|Deep neural network|[Github](https://github.com/rani700/molecules_classification/blob/master/musk-vs-non-musk/deep-neural-network/training.ipynb)  [Colab](http://colab.research.google.com/github/rani700/molecules_classification/blob/master/musk-vs-non-musk/deep-neural-network/training.ipynb)  [model.h5](https://github.com/rani700/molecules_classification/blob/master/musk-vs-non-musk/deep-neural-network/model_dnn.h5)|[Github](https://github.com/rani700/molecules_classification/blob/master/molucule-classification/deep-neural-network/training.ipynb)  [Colab](http://colab.research.google.com/github/rani700/molecules_classification/blob/master/molucule-classification/deep-neural-network/training.ipynb)  [model.h5](https://github.com/rani700/molecules_classification/blob/master/molucule-classification/deep-neural-network/model_molecule_dnn.h5)|
|Convolutional neural network|[Github](https://github.com/rani700/molecules_classification/blob/master/musk-vs-non-musk/convolutional-neural-network/training.ipynb)  [Colab](http://colab.research.google.com/github/rani700/molecules_classification/blob/master/musk-vs-non-musk/convolutional-neural-network/training.ipynb)  [model.h5](https://github.com/rani700/molecules_classification/blob/master/musk-vs-non-musk/convolutional-neural-network/model_musk_vs_non_musk_cnn.h5)| [Github](https://github.com/rani700/molecules_classification/blob/master/molucule-classification/convolutional-neural-network/training.ipynb)  [Colab](http://colab.research.google.com/github/rani700/molecules_classification/blob/master/molucule-classification/convolutional-neural-network/training.ipynb)  [model.h5](https://github.com/rani700/molecules_classification/blob/master/molucule-classification/convolutional-neural-network/model_molecule_cnn.h5)|
|Transfer learning|[Github](https://github.com/rani700/molecules_classification/blob/master/transfer-learning/training.ipynb)  [Colab](http://colab.research.google.com/github/rani700/molecules_classification/blob/master/transfer-learning/training.ipynb)  [model.h5](https://github.com/rani700/molecules_classification/blob/master/transfer-learning/model_musk_vs_non_musk_transfer_learning.h5)| |



