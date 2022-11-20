# Between-Class learning for Image Classification

This is an extension of the Between-Class learning model proposed by (Tokozume, 2018).
This paper intends to explore the novel Between-Class mixing algorithm for the CIFAR-10 dataset.

However, instead of training the model to output the mixing ratio of the two classes we 
are simply training the model to output the class of the image which has the higher mixing ratio


## Run Locally

Clone the project

```bash
  git clone https://github.com/KennethWrong/Between-Class-Learning.git
```

- From the project directory ECE57000_project.ipynb contains all the code.
- Choose to run the notebook either on google colab **(Perferred)** or run it locally on jupyter notebook



## Acknowledgements

- [**CIFAR-10**](https://pytorch.org/vision/stable/generated/torchvision.datasets.CIFAR10.html)
  - The CIFAR-10 dataset was imported from torchvision in the datasets module. I imported the dataset and made my own changes through transformations and mixing with either BC or BC+ mixing algorithm. 

- [**Pytorch Resnet-18**](https://pytorch.org/vision/master/models/generated/torchvision.models.resnet18.html)
  - The Resnet-18 model was imported from the official pytorch implementation.

- [**Convnet**](https://github.com/mil-tokyo/bc_learning_image)
  - The Convnet models architecture is taken from the [original paper's github repository](https://github.com/mil-tokyo/bc_learning_image) I had to reimplement the architecture using Python3 and pytorch as the original paper used Chainer and Python2.X.

- [**Shake-Shake Regularization**](https://notebook.community/t-vi/pytorch-tvmisc/misc/cifar10-shake-shake)
   - For this model I imported the code from a notebook of a quick implementation of the Shake-Shake Regularization model. I did not make any changes but I selected the model to have a depth of 8.

- **Training and Testing functions**
  - Code For training and testing the models is taken from Purdue's ECE57000 Assignments.

## Results

### Image preprocessing steps
![Image of preprocessing process](https://github.com/KennethWrong/Between-Class-Learning/blob/main/images/preprocess.png?raw=true)

### Example of images after preprocessing and mixing
![Example of images after preprocessing and mixing](https://github.com/KennethWrong/Between-Class-Learning/blob/main/images/image_transform.png?raw=true)

### Accuracy of models after training with various mixing algorithms
![Accuracy of models after training](https://github.com/KennethWrong/Between-Class-Learning/blob/main/images/result_table.png?raw=true)

### Loss of model trained with BC mixing algorithm
![Loss of models trained over BC mixing algorithm](https://github.com/KennethWrong/Between-Class-Learning/blob/main/images/bc_loss.png?raw=true)

### Loss of model trained with BC+ mixing algorithm
![Loss of models trained over BC+ mixing algorithm](https://github.com/KennethWrong/Between-Class-Learning/blob/main/images/bc_plus_loss.png?raw=true)

