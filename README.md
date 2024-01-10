# Cancer-cell-classification-w-ConvNets
 This is a coursework of the Deep Learning class from my Data Science master's degree. The overall goal for this coursework is to train **two deep neural networks** which can take 100x100 pixel images with a cell nucleus in the centre of the image and classify it into one of the following types which are shown in the figures above:  <br>

1. Normal epithelial cell nuclei with label 0.
2. Cancer epithelial cell nuclei with label 1.
3. Muscle cell nuclei with label 2.
4. Immune leukocyte cell nuclei with label 3.<be>


## Notebook Overview
This coursework was implemented on the Kaggle notebook with the GPU P100 config. Notable libraries used include `torch`, `torchvision`, `sklearn` and more. Overall workflow as demonstrated in the notebook is as follows:
1. **data preprocessing** - _dealing with class imbalance, custom dataset class, data transformation, load data to dataloader_
2. **modeling** - _building 2 CNN models, one small model from scratch and one modified ResNet18, defining train function & running the training_
3. **interpreting the models** - _loss and accuracy curves, confusion matrix, Captum_
4. **hyperparameter tuning** - _using ray library to tune the learning rate, weight decay and momentum, define new training function_
5. **final model** - _brief evaluation, generating predictions using the final model_
6. **future enhancement** - suggestions include data augmentation, early stopping, ray library, closer look at model1 <be>


## Data file descriptions
* `train.zip` - zip file containing the training images
* `test.zip` - zip file containing the test images
* `train.csv` - csv file containing the training image filenames and ground truth labels (0, 1, 2, 3)
* `example.csv` - an example submission file in the correct format <br>

## Data fields
* `Filename` - filename of an image file.
* `Label` - the type of cell nucleus in the middle of the image.

