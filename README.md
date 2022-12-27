# Flower-Images-Classification
A Flower Images Classification using Deep Neural  Network Models

## Problem Statement
  There are flowers everywhere around us. In addition to providing a home for almost all insect pollinators 
  and being beautiful decorations for homes and gardens, they are regarded as the most crucial part of the food chain.
  They are also used in the medical field to treat people and some animals. Flowers grow in a wide variety around the world,
  making them incredibly complex, time-consuming, and difficult for even highly experienced gardeners to identify their species
  manually. Therefore, owning adequate recognition of flower species is essential for quick and accurate flower classification 
  which will be useful in various commercial, medicinal, and agricultural domains.

## Dataset
  Firstly, we collected unlabeled 500 flower images of ten from different resources on the internet and each class has 50 images. 
  All images resized to be 64*64 Pixels.
 ![image](https://user-images.githubusercontent.com/95842589/209652338-73788e27-f81b-4cff-a71c-efdebc7c2a31.png)

  A. Dataset structure
    The dataset used in this project was manually collected by the authors from various online sources and consists of 10 
    classes ['Azalea', 'Peony', 'Rose', 'Sunflower', 'bellflower', 'calendula flower', 'daisy', 'dandelion', 'marigold', 'tulip'], each 
    class referring to a type of flower. we organized it into training, validation, and testing.
    A total number of images are 500 were collected and then split by a ratio of 80%-20% among the training and 
    validation/test sets, where 400 images were used for training, 50 images for validation, and 50 for testing. Each category of 
    flowers was in a different file.In general, the dataset was ensured to have variations in 
    the shape of the images in brightness, contrast, background, and angles to allow the learnability of the model under 
    different conditions.
  B. Preprocessing
    Since some of our images are less than 64*64, we had to 
    perform some transformations in order to make all of our 
    images the same size for modeling.
  C. Data Augmentation
    Since we have a very small dataset, we applied data 
    augmentation techniques. we took each of our training images 
    and applying different augmentation technique to perform 
    transformations. The sample images of each category before 
    applying data augmentations can be seen in fig.1. and the 


## Methodology
  We applied different pretrained CNN models like VGG-16 and DenseNet201 and then compare their results to each other to decide which 
  one will be compatible with this case and every model we trained with and without data augmentation. We used python language and Pytorch
  framework for the implementation.
  
![image](https://user-images.githubusercontent.com/95842589/209652265-d58cd171-0b3b-4852-8216-db78ac5601a5.png)

## Results
  Believing in the importance of flowers in human life,  we developed a model that can classify 10 different categories of flowers from images.

   -- VGG16

![image](https://user-images.githubusercontent.com/95842589/209653204-23851270-68e2-4819-ba91-c5860a108377.png)

  -- DensNet201

![image](https://user-images.githubusercontent.com/95842589/209653539-3f1e9e6a-2130-4a36-bcd0-d1d31851e5f1.png)

  Comparing results:

![image](https://user-images.githubusercontent.com/95842589/209653378-e04bec4f-c0fc-4451-9f92-c11decac8859.png)

## CONCLUSION

we have presented our work in classifying images that involve ten different types of flowers. We have also presented our
efforts in collecting diverse images to make our final dataset and the pipeline we followed in our 
experiments, we have also increased our model’s performance by using data augmentation through four different 
augmentation techniques. Finally, we evaluated our experiments for model comparison, determine the best model, 
and define our next steps to be considered for future work. The proposed solution achieves a testing accuracy of 82% and an 
average F1 score of 81%, as shown from the previous results we had got in our work that increasing the complexity and 
depth of artificial neural networks for the classification problem is not always a better solution for all cases, since 
when using the small sized images like in our case, and increasing in the number of layers will lead to the model will 
be overfitting and that can be observed in the densenet201 model training and validation curve as the early stopping 
stopped the model after 25 epochs only on the other hand in the VGG16 model it stopped after 36 epochs and VGG16 had 
higher accuracy compared with the DenseNet201 after applying data augmentation on our dataset.





