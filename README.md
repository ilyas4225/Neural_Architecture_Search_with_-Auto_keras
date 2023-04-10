# Neural_Architecture_Search_with_-Auto_keras

Neural architecture search is a technique that automates the designing of neural networks for solving a particular problem. Auto-Keras is a framework for automated machine learning (AutoML), which includes support for neural architecture search (NAS) for deep learning models.Auto-Keras provides an easy-to-use interface for searching for the best neural network architecture for a given task.


## Requirments  

 ```
!pip install autokeras
```
## Developing a Classifier Using Auto Keras
In this section, we will build a classifier on the the different data sets like Cifar100,Cifar10, MNIST,DTD,STL10 dataset because of the simplicity of the dataset as well as because the search takes a long time to run so the simpler the dataset the simpler it is to search for the best parameter.

## Notebook description
In this repository the notebook ['[autoModel_Cifar100.ipynb'](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/autoModel_Cifar100.ipynb)] contains the autokeras image classifier for cifar100 dataset.


The Cifar10 notebook ['[cifar10_Notebook .ipynb'](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/cifar10_Notebook%20.ipynb)] contains the auto keras classification with  image classifier, customized search space with ResNet architecture with Cifar10 dataset.


This third notebook in the repository ['[mnist_STL10_DTD.ipynb](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/mnist_STL10_DTD.ipynb)] contains the auto keras classification on the mnist, STL10,DTD dataset with  image classifier, customized search space with ResNet architecture.

## Result Discussion
###Results with AutoModel
The AutoModel is initialized with the defined input and output nodes, and trained on the CIFAR-100 dataset for 2 epochs and max_trials  are 2. 
['[autoModel_Cifar100.ipynb'](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/autoModel_Cifar100.ipynb)] 
The architecture discovered by the AutoModel is a combination of ResNet50 feature extractor and a few Dense layers for classification. The exact architecture can be seen in the summary of the exported model:


 ![1](https://user-images.githubusercontent.com/101690101/230955044-76d27e7f-134a-40b6-b0ab-d7b2c8f4ab45.png)


