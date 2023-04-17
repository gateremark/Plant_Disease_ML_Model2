# Plant Disease Detection using MobileNetV2

This repository contains a Python script for building a plant disease detection model using MobileNetV2, a pre-trained model in Tensorflow Keras. This project aims to classify plants into their respective disease categories, thus helping farmers detect plant diseases early and take necessary preventive measures.

## Dataset

The dataset used for this project is the [PlantVillage Dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset). It contains over 54,000 images of healthy and diseased plants in ~40 different classes that can be used for developing machine learning models.

## Usage

Before running the script, you need to mount Google Drive to access the dataset files. After mounting it, run the following command to extract all the files:

```python
!unzip /content/drive/MyDrive/Digitalfarmer/PlantVillage.zip
```

After extracting the files, set the directories for the training and validation data sets and some global constants. Then, create image data generators with data augmentation options and save the dataset labels.

Prepare MobileNetV2 by setting its weights, discarding the last 1000 layers with softmax activation for use in ImageNet, and adding the desired layers for our classification task. Fine-tune the model and compile it with an optimizer, loss function, and metrics. Train the model using the fit() function and callbacks for saving the best model and stopping early if needed. Finally, plot the training accuracy and loss along with the validation accuracy and loss and save the best model as pdd_mobilenet2_v1.h5.

You can use the get_prediction() function to predict the class of a given image using the saved model and print the predicted class.

## Credits

The PlantVillage Dataset and the MobileNetV2 pre-trained model in Tensorflow Keras are used for this project. Special thanks to [Victor Ndaba](https://github.com/ndaba1) for making this project possible.

## License

This project is licensed under the [MIT](https://opensource.org/licenses/MIT) license. Feel free to use it for educational or commercial purposes.
