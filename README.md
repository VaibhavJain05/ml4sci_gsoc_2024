# Ml4SCI_GSOC_2024

## Learning Representation Through Self-Supervised Learning on Real Gravitational Lensing Images
#### **Description** :

Strong gravitational lensing is a promising probe of the substructure of dark matter to better understand its underlying nature. Deep learning methods have the potential to accurately identify images containing substructure, and differentiate WIMP particle dark matter from other well-motivated models, including axions and axion-like particles, warm dark matter etc.

Supervised classification can be difficult when the number of known objects of a particular class is very small. This is usually the case for strong gravitational lensing images, where the number of samples from one or more classes are relatively lower than others. Self-supervised learning (SSL) has proven to outperform standard supervised machine learning models, particularly when the number of data labels available for supervision is low. Moreover, SSL can take advantage of very large unlabelled datasets that would be difficult or impossible to label manually and build meaningful representations. To date, only convolutional neural networks (CNNs) have been used with the SSL technique for strong gravitational lensing data. Transformers or hybrid models (Transformers + CNN) promise more robustness for representation learning but have not been addressed by the community. This project will focus on the development of self-supervised learning techniques with Transformers for strong gravitational lensing data on real dataset


## Common Test I. Multi-Class Classification:
I have used ResNet18 for the common task and got a ROC AUC score of 0.99 on testing/validation.

Model weights: [LINK](https://drive.google.com/drive/folders/1A50EkrU-exz64wKhicDIUclrhLCbZ-9P)

## Specific Test VI. SSL on Real Dataset:
For, self supervised task, I have used the ResNet18 as backbone and a linear classifier for evaluation. The approach I took is from the SimCLR v1 paper. I got a ROC AUC score of 0.5536 on testing data.

I have splitted the dataset into 3 parts 60:30:10(overall training 90, testing 10) for pre-training, fine-tuning and testing phase.
Since the dataset was very less (215 images), the low ROC AUC score was expected, but with the increment in the dataset, we will surely see a significant increase in the metric and the performance of the model.

Model weights: [LINK](https://drive.google.com/drive/folders/1zrtvLE1-HoSskYjwyI-KAJGfk4L_F1pp)

## **All the code and scripts used are added in the folders. Each folder has a instruction file which is used to access the weights and results of the evaluation tasks.**
