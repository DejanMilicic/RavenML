# RavenML

How to use Machine Learning with RavenDB

## Emotion Analysis of employee photos

1. Train Model that will recognize human emotions on images
2. Use it with RavenDB index as an external source

## Training the model

Starting with one of the basic examples of [Image Classification](https://github.com/dotnet/machinelearning-samples/tree/master/samples/csharp/getting-started/DeepLearning_ImageClassification_Training) we can see the basic idea - we tag set of images, and those tagged images are used as a model that ML.NET 
will use to train model.  
Trainging data [setup](https://github.com/dotnet/machinelearning-samples/tree/master/samples/csharp/getting-started/DeepLearning_ImageClassification_Training/ImageClassification.Train/assets/inputs/images/flower_photos_small_set) is very simple - each category is represented by 
the folder containing sample images. Folder names will be used as a category labels, and content of each folder will be used to train ML.NET model to recognize 
images from that category.

Since this training example deals with flowers, we need to replace images of the flowers with pre-classified dataset of images showing basic human emotions.  
There is a very nice article [Emotion Analysis with building an Artificial Neural Network using ML.NET with Tensorflow](https://medium.com/analytics-vidhya/emotion-analysis-with-building-an-artificial-neural-network-using-ml-net-powered-by-tensorflow-dd08aeb9aad7) with complete [source code](https://github.com/y3n3rrr/EmotionAnalysisWithMLNET) 
published on GitHub, including set of [training images](https://github.com/y3n3rrr/EmotionAnalysisWithMLNET/tree/master/assets/inputs/images).
