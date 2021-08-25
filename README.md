<h1> GTSRB-traffic-sign-recognition </h1>
Deep learning model to recognize traffic sign trained using GTSRB dataset.

The SampleImages folder containes the sample train and test images. in the Training folder the images with the prefix aug are augmented samples, they are not available with the
original GTSRB dataset.

<p align="center">
  <img src="https://benchmark.ini.rub.de/material/0.png" />
  <img src="https://benchmark.ini.rub.de/material/1.png" />
  <img src="https://benchmark.ini.rub.de/material/2.png" />
  <img src="https://benchmark.ini.rub.de/material/3.png" />
  <img src="https://benchmark.ini.rub.de/material/4.png" />
  <img src="https://benchmark.ini.rub.de/material/5.png" />
  <img src="https://benchmark.ini.rub.de/material/6.png" />
  <img src="https://benchmark.ini.rub.de/material/7.png" />
  <img src="https://benchmark.ini.rub.de/material/8.png" />
  <img src="https://benchmark.ini.rub.de/material/9.png" />
  <img src="https://benchmark.ini.rub.de/material/11.png" />
</p>
  
DataPrep.ipynb --> The program is used to convert the .ppm images to .bmp to make it easy for tensorflow to process tha images.

DataAug.ipynb --> Uses albumentations library to create the augmented images and also balance the dataset refer images Augmented and unAugmented to check the difference the
number of samples in each class.

<h3><center>Samples per class before augmentation</center></h3>

<p align="center">
  <img src="/UnAugmented.png" />
</p>

### Samples per class after augmentation
<p align="center">
  <img src="/Augmented.png" />
</p>

Model.ipynb --> Contains the model structure and the training process. The acuuracy and loss can be visualized in the respective image file, Accuracy and loss
### Accuracy change across 50 epochs
<p align="center">
  <img src="/Accuracy.png" />
</p>
### Loss change across 50 epochs
<p align="center">
  <img src="/loss.png" />
</p>

Evaluation.ipynb --> Contains the model evaluation using the GTSRB test dataset, the accuracy of the model was near 97% on the test data. The confusion matrix can also be
visualized in the image file, Confusion_Matrix.
### Confusion Matrix
<p align="center">
  <img src="/Confusion_Matrix.png" />
</p>

The Saved_ephocs_v3.0 folder contains the weights of the model.

The complete train and test dataset can be downloaded from https://sid.erda.dk/public/archives/daaeac0d7ce1152aea9b61d9f1e19370/published-archive.html

Reference:
J. Stallkamp, M. Schlipsing, J. Salmen, C. Igel, Man vs. computer: Benchmarking machine learning algorithms for traffic sign recognition, Neural Networks, Available online 20 February 2012, ISSN 0893-6080, 10.1016/j.neunet.2012.02.016. (http://www.sciencedirect.com/science/article/pii/S0893608012000457) Keywords: Traffic sign recognition; Machine learning; Convolutional neural networks; Benchmarking
