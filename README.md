## Unsupervised Domain Adaptation-UDA

Proposing a Unsupervised Domain Adaptation-UDA technique to counteract the negative impact of the domain gap when training the model on the source distribution and evaluating it on the target distribution. As it holds for any standard UDA framework, the quality of the domain alignment strategy shall essentially be assessed by looking at the gain obtained with the proposed framework over the so called source-only baseline. Here DialNet is used a baseline architecture. The accuracy is improved by using AlexNet and ResNet network

## Dataset

Adaptiope, a widely used object recognition dataset with public access. This dataset comprises images from three distinct domains, refering to synthetic, product, and real world data. The original sataset comprises 123 object categories in each domain. 20 categories were extracted randomly from the product and real world domains in this experiment.

## Implementation
* Train the model supervisedly on the source domain, i.e. having access to the images as well as the object labels
* Train the model unsupervisedly on the training set of the target domain, i.e. having access to the images, but not to the labels
* Evaluate the model on the test set of the target domain

The adopted domain alignment strategy is generally evaluated with respect to the gain that it enables over the source-only performance. As the name suggests, the source-only baseline that should be taken into account when evaluating any UDA framework simply consists of the score obtained when training the model on the source domain and evaluating it on the target domain, without any domain alignment strategy involved. The more effective the chosen domain alignment strategy is, the higher the gain will be over the source-only version. The implementation is as following

To recognize object a DIALNET network was used as a baseline architecture. Utilized the weights to test the model in the target domain after training it in the source domain to determine its accuracy and gain. In baseline network the accuracy was low and the gain was small. Updated the pipeline adding AlexNet network with the baseline architecture. Trained the model again in the source domain and tested it into the target domain. The accuracy was increased compared to the before as well as the gain also. 

## Extension of the work.
To get the better accuracy the pipeline was updated once by adding the ResNet network with previous architecture. After training the model the accuracy was increased by 90% which is a standard one. In every step the gain is calculated by subtracting the value of accuracy of Domain Adaptaion from the value of Source accuracy.

## Domain Shifting
Training and testing the model was in two direction. The model was trained by making the Real World data as a source domain and product data as a target domain. Then the process was alter by making the product data as a source domain and Real World data as a target domain. The accuracy and gain was high during the training model from Real World domain to Product domain.

## Complete report
[Notebook](https://github.com/azgarshuvo/unsupervised-domain-adaptation/blob/main/unsupervised-domain-adaptation.ipynb)
