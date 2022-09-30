## Unsupervised Domain Adaptation-UDA

Proposing a Unsupervised Domain Adaptation-UDA technique to counteract the negative impact of the domain gap when training the model on the source distribution and evaluating it on the target distribution. As it holds for any standard UDA framework, the quality of the domain alignment strategy shall essentially be assessed by looking at the gain obtained with the proposed framework over the so called source-only baseline. Here DialNet is used a baseline architecture. The accuracy is improved by using AlexNet and ResNet network

## Dataset

Adaptiope, a widely used object recognition dataset with public access. This dataset comprises images from three distinct domains, refering to synthetic, product, and real world data. The original sataset comprises 123 object categories in each domain. 20 categories were extracted randomly from the product and real world domains in this experiment.

## Implementation
* Trained model supervisedly on the source domain, i.e. having access to the images as well as the object labels
* Trained model unsupervisedly on the training set of the target domain, i.e. having access to the images, but not to the labels
* Evaluated the model on the test set of the target domain

To recognize object we used a DIALNET network as a baseline architecture. We utilized the weights to test the model in the target domain after training it in the source domain to determine its accuracy and gain. In baseline network the accuract was low and we got small gain. Then we used AlexNET and connect the features with the in feature of Baseline architecture by the fully connected layer. We got a better accuracy rather than before. Finally, at the extension part of the implementation we added RESNET network and got 90% accuracy of the domain adaptation techniques. 
