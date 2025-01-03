# Brain Tumor Detection using Deep Learning

## Introduction

The human brain is the major controller of the humanoid system. The abnormal growth and division of cells in the brain lead to a brain tumor, and the further growth of brain tumors leads to brain cancer. In the area of human health, Computer Vision plays a significant role, which reduces the human judgment that gives accurate results. CT scans, X-Ray, and MRI scans are the common imaging methods, among which magnetic resonance imaging (MRI) is the most reliable and secure. MRI detects even minute objects.

Our project aims to focus on using different techniques to discover brain cancer using brain MRI. We utilize a deep learning approach, specifically Convolutional Neural Networks (CNNs), to automatically analyze MRI scans and predict the presence or absence of brain tumors. Early and accurate tumor detection is crucial for effective treatment and improved patient outcomes.

## Dataset

The project utilizes a dataset of brain MRI scans, divided into two classes: "tumor" and "no tumor." The images were preprocessed to enhance the features relevant to tumor detection.

* Dataset Source: [Dataset]
* Number of Images: [Total number of images in the dataset](https://drive.google.com/drive/folders/1LPJI-kJ6TbWDZvHf0U5nDVgks1afinaa)
* Preprocessing Steps: 
    * Image resizing to a uniform size.
    * Normalization of pixel values to a specific range.
    * Data augmentation techniques (rotation, flipping, brightness adjustments) to increase the dataset size and improve model robustness.


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

1.  Clone the repository.
2.  Install the required dependencies: `pip install -r requirements.txt`.
3.  Run the code: `python main.py`.

## Contributing

Contributions are welcome! Please follow the guidelines outlined in [CONTRIBUTING.md].

## License

This project is licensed under the MIT License.
