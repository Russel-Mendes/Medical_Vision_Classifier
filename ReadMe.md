# Utilizing a Keras Classifier to Aid in Disease Identification

As Machine Learning becomes more effecient and more available to the masses, there more applications for the technology in many fields. One such field is medicine. Within this field, doctors, surgeons, paramedics, and other members need years of expertise to effectively treat their patient. Few tools such as WebMD and the Mayo Clinic make valuable medical data available to the layman in an easy format. Nonetheless, to utilize these tools effectively, the user has to have to have a sense of the illness at hand. In order to aid the enter general public, machine learning can be used. Instead of relying on an individual's latent knowledge on a disease, machine learning can use information of disease to identify and offer an appropriate treatment.  

The goal of this project is to utilize a Keras Image Classifier to identify diseases. After identifying the disease, the program will take the identified class and search in a database for an appropraite response. The response will compose of treatment, cause, and lenght. This classifier will try to classify the following wound types: 
- Lacerations 
- Abrasion
- Avulsion
- Punctures
- Contusions. 

This project utilizes the architecture of the VGG16 Model. The VGG16 is a 16 layer convultional deep network that was originally trained on ImageNet. For this project, only the architecture will be used and the weights will be trained using medical images. 

## Important Components

When downloading there are three main things that are important in this repository:
- Data Augmenter: This jupyter notebook has two functions that augments images, expanding our data set.
- Data: This is a collection of 1200+ images that is already split into labelled classes
- Medical Vision Classifier: This is the FineTuned and trained VGG16

### Prerequisites
This machine learning project uses the following libraries and modules:

-Keras 2.2.2
-Tensorflow 1.8.0
-Numpy 1.14
-Matplotlib 2.2.2
-itertools
-Pillow 5.2.0

### Installing the Previous Dependencies

This project installed Anaconda, which installs the majority of the dependencies. The only things not installed is Tensorflow and the Keras wrapper

To install the latest version of Keras, simply input the following line in the command prompt
```
pip install Keras
```
If you want a specific version of Keras:
```
pip install Keras==x.x.x
```
Tensorflow can be installed by following this official link: https://www.tensorflow.org/install/
## Current Performance
As of 8/18/2018, and with a data set of roughly 1200 images, the model has an accuracy of 98% and a validation accuracy of 70% after 100 epochs. However, when using the test data set, and as seen in the confusion matrix, Out of 191 tested images, 44 images were classified correctly. The area with the largest missclasification is the contusion category. This indicates few possible problems. First, the data may be diry, or bad. Second, the data may be baised towards contusions. Third, the data set may be to small regarding its test images. Fourth, the model may have been overfitting, even though it is not apparently seen. Overall, these problems can be rectified by simply expanding the data set, perferabely with the goal that every category has roughly the same image count and quality. 
**Review**
-98% accuracy
-70% validation accuracy 
-23% accuracy with the test data set
-Possible fix is to expand the size and quality of data set

## Contributing
Anyone who wants to contribute to this project is freely allowed to. Just make sure to give due credit -- such as a hyperlink-- and read the disclaimers.

## Known Bugs
Currently there are few bugs within this project. 
- The Data Augmentation functions when given extreme amounts images to iterate it will struggle to convert file types. 
- The Data Augmentation functions may have trouble recognizing some images.
- As of this publishing, Keras 2.2.0+ has a known issue regarding its ability to load models. A method to fix this downgrading to a Keras 1.1.x model. 
## Version
Due to the bugs caused by Keras 2.2.2, this project is on version **0.9.0**
## Author
* **Russel Mendes** 
## **Disclaimer**
- The Data used in this project are sourced through Google Images. These images are fine according to the Creative Commons License; thus it is advised from not using these images for commercial applications. 
- The images used in the Data is composed of real medical injuries. Therefore, a warning must be issued regarding the mature contant inside.  

## Acknowledgments
* DeepLizard and Siraj Raval gave me inspiration for this project
