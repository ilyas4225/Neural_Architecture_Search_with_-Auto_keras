# Neural_Architecture_Search_with_Auto_keras

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

### Results with AutoModel
The model discovered by AutoKeras for the CIFAR-100,cifar10,STL10 dataset has a series of convolutional and dense layers, as well as dropout and normalization layers. The architecture of the model can be seen in the summary provided below

The architecture discovered by the AutoModel is a combination of ResNet50 feature extractor and a few Dense layers for classification. 

| Dataset  |Autokeras_searching_class|max_trail | Epochs|Accuracy|
|----------|-------------------------|----------|-------|--------|
| Cifar100 | AutoModel               | 2        |2      | 0.89%  |
| Cifar10  | AutoModel               | 2        |2      | 42.57% |
| STL10    | AutoModel               | 2        |10     | 10.00% |

#### The exact architecture can be seen in the summary of the exported model on Cifar100:

![](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/images/Cifar100_auto.png "AutoModel_Cifar100")

#### The architecture Summary on Cifar10:

![](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/images/cifar10_auto_model.png "AutoModel_Cifar10")

#### The architecture Summary on STL10:

![](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/images/STL10_auto_model.png "AutoModel_ST10")


### Results by Customized Search Space
Customized search space in AutoKeras refers to the ability to define a specific set of possible model architectures and hyperparameters that AutoKeras should explore during its search for the best model for a given task.
Here the search space is set to "resnet" to restrict the search space to only ResNet architectures.  Search space for AutoKeras to find an optimal image classification model using ResNet architectures.

| Dataset  |Autokeras_searching_class|max_trail | Epochs|Accuracy|
|----------|-------------------------|----------|-------|--------|
| Cifar10  | ResNet                  | 1        |10     | 44.12% |
| mnist    | ResNet                  | 1        |10     | 98.55% |
| DTD      | ResNet                  | 2        | 5     | 2.13 % |



#### The architecture Summary on Cifar10 when searching space is customized with resnet:

![](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/images/cifar10_customized.png "resnet_cifar10")


#### The architecture Summary on DTD when searching space is customized with resnet:

![](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/images/DTD_Customized%20search.png  "resnet_DTD")


### Results by Ak.classifier

| Dataset  |Autokeras_searching_class|max_trail | Epochs|Accuracy|
|----------|-------------------------|----------|-------|--------|
| Cifar10  | ak.ImageClassifier      | 1        |10     | 73.49% |
| mnist    | ak.ImageClassifier      | 1        |10     | 98.87% |
| STL10    | ak.ImageClassifier      | 1        |10     | 56.87% |

#### The architecture Summary on STL10 with Ak.imageclassifier:

![](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/images/STL10_img_clf.png "STL10_ak_clf")

#### The architecture Summary on Cifar10 with Ak.imageclassifier:

![](https://github.com/ilyas4225/Neural_Architecture_Search_with_-Auto_keras/blob/main/images/cifar10_ak_clf.png "cifar10")




