# Boat Type Classification

Suggested algorithm to classify marine vessels from images using ResNet50 for feature extraction and LDA model for classification.  

## Introduction: 
Small marine vessels are very common, these vessels usually don’t have many mechanical tools or electronic communication devices.  
When these marine vessels are in distress in open water the most efficient option available to them is to activate a distress signal.
The goal of our algorithm is to recognize the types of the distressed vessels in real time. So that when a distress signal is received, the algorithm can report the type of vessel involved and save valuable time. 
The existing algorithms are based on artificial neural networks and/or different linear classifiers. Their accuracy ranges between 76-82%. 
The algorithm we implemented works as follows: The algorithm receives photos of distressed marine vessels, these photos will be processed by a pretrained neural network. After the data passes the appropriate layers, a number of features are extracted and are run through a LDA classifier which classifies the type of marine vessel.

The algorithm was trained on a data set of 2865 (Visible images and InfraRed images) pictures which contain 6 different types of vessels. The photos where processed by a set of functions so the data will fit as input for the algorithm. We changed the size but kept the proportions of the photos, and we increased the color range in each photo.
After training the algorithm we tested the algorithm on photos that were not part of the training set. The algorithm classified correctly 90% of the small vessels and 93% of the sail boats.

## System Architecture:
![image](https://user-images.githubusercontent.com/62745598/178217996-72f0aec9-8da6-4b14-979f-3ed834801b7c.png)  
![image](https://user-images.githubusercontent.com/62745598/178218083-9afb3986-7070-4f16-900d-f9cfbaa66d85.png)


## Results:
### Visible images confusion matrix:  
![178218542-cef9aa7f-13c9-4ab1-bbcc-b20f5f1d856a](https://user-images.githubusercontent.com/62745598/178218870-f19c7077-1721-48c4-92e3-b9fe0d9e26ad.jpeg)

### InfraRed images confusion matrix:  
![download](https://user-images.githubusercontent.com/62745598/178219034-91d54155-cdcb-4f2f-bc66-b196d188b5c1.jpeg)


