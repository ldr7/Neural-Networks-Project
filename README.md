# Artificial-Neural-Networks-Course-Project  

## Objective  
To classify images in the MNIST dataset using coeffcients from the 2-D DWT of the image. Further, investigate the efficacy of the 4 different coefficients obtained from the 2-D DWT for the purposes of image classification.  
  
## Approach   
Nominal pre-processing is done and the class labels are converted to binary from categorical. 'db38' wavlet is used to perform the 2-D DWT of the image, which generates 4 sets of coefficients- cA,cV,cH,cD. Here cA is the approximate coefficients and cH,cV,cD are coeffcients in the horizonatal, vertical and diagonal directions respectively. 4 CNN models are created to classify the images. These models use the different coefficents obtained from the DWT.  
  
## Results
It is observed that the model using cA gives the highest accuracy followed by models using cV,cH and cD respectively. This hints that the vertical axis might be more useful in classification of MNIST images.  
However, cA is clearly ahead of the other coefficents in terms of efficacy for classification of MNIST images. Another model is built that polls the 4 models, weighted as per their test accuracies. As expected, this model performs worse than the model using cA but better than the models using the other coefficents.  
  
## Techologies  
  
The project uses the following: 
  
* Python3  
* Jupyter Notebook  
* pywt (python wavlet package)  
* keras  
* numpy
