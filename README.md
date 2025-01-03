# Brain Tumor Detection using Deep Learning

## Introduction

The human brain is the major controller of the humanoid system. The abnormal growth and division of cells in the brain lead to a brain tumor, and the further growth of brain tumors leads to brain cancer. In the area of human health, Computer Vision plays a significant role, which reduces the human judgment that gives accurate results. CT scans, X-Ray, and MRI scans are the common imaging methods, among which magnetic resonance imaging (MRI) is the most reliable and secure. MRI detects even minute objects.

Our project aims to focus on using different techniques to discover brain cancer using brain MRI. We utilize a deep learning approach, specifically Convolutional Neural Networks (CNNs), to automatically analyze MRI scans and predict the presence or absence of brain tumors. Early and accurate tumor detection is crucial for effective treatment and improved patient outcomes.

## Dataset

The project utilizes a dataset of brain MRI scans, divided into two classes: "tumor" and "no tumor." The images were preprocessed to enhance the features relevant to tumor detection.

* Dataset Source: [Dataset](https://drive.google.com/drive/folders/1LPJI-kJ6TbWDZvHf0U5nDVgks1afinaa)
* Preprocessing Steps: To enhance model performance, the dataset is preprocessed using techniques such as:
*  **Rescaling:** Pixel values are normalized to a range of 0-1.
* **Grayscaling:** Images are converted to grayscale to reduce complexity.
* **Data Augmentation:**  The training dataset is augmented using techniques like rotation, shifting, and flipping to increase its size and variability. This helps the model generalize unseen data better.



## Methodology

A CNN-based approach is employed for image classification. The model architecture consists of multiple layers, including convolutional layers, pooling layers, and fully connected layers. The model was trained using the RMSprop optimizer and the categorical cross-entropy loss function for a specified number of epochs.

**Preprocessing:**
*  We performed pre-processing using the bilateral filter (BF) for the removal of noise present in the MR images.
*  Binary thresholding was applied to segment the tumor region from the background.
*  CNN segmentation techniques were utilized for reliable detection of the tumor region.

**Model Architecture:**
* Input Layer: Grayscale images of size (200, 200, 1).
* Convolutional Layers: Multiple convolutional layers with varying filter sizes and activation functions (ReLU).
* Pooling Layers: Max pooling layers to reduce dimensionality and extract dominant features.
* Dropout Layers: Dropout layers to prevent overfitting.
* Flatten Layer: Converts the multi-dimensional feature maps into a single vector.
* Dense Layers: Fully connected layers for classification.
* Output Layer: Softmax activation function to predict the probability of tumor presence.

**Training Process:**
* The dataset was divided into training, testing, and validation sets.
* The model was trained using the training set and validated using the validation set.
* Performance metrics were evaluated on the testing set.

## Results

The trained model achieved an accuracy of [98.85]
## Discussion

Based on our model, we can predict whether a subject has a brain tumor or not. The resultant outcomes were examined through various performance metrics, including accuracy, sensitivity, and specificity. It is desired that the proposed work would exhibit exceptional performance compared to existing methods.

**Limitations:**
* The model's performance may be affected by the quality and diversity of the training data.
* Further evaluation on larger and more diverse datasets is necessary to assess the model's generalization ability.

**Future Directions:**
* Explore the use of advanced deep learning architectures and techniques to improve accuracy and robustness.
* Develop a user-friendly interface for deploying the model in clinical settings.
* Investigate the potential of using the model for tumor segmentation and classification into different subtypes.

## Usage

1.  Clone this repository to your local machine.
2.  Install the required libraries: `pip install tensorflow keras pandas numpy matplotlib seaborn scikit-learn pillow opencv-python`
3.  Mount your Google Drive to access the dataset:  Refer to the 'PATH PROCESS' section in the notebook for instructions on mounting Google Drive and setting the dataset paths.
4.  Run the Jupyter notebook or the Collab to train and evaluate the model.
## Contributing

Contributions are welcome! Please follow the guidelines outlined in [CONTRIBUTING.md].

## License

This project is licensed under the MIT License.
