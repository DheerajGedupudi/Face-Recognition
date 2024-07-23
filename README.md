# Face Recognition System using ResNet50

## Project Overview
This project was developed as part of the COEN 240 Machine Learning course at [Santa Clara University](https://www.scu.edu/). The aim was to build a face recognition system that is as accurate as possible. We could choose any model, from SVMs to deep learning algorithms. I chose to use a pre-trained ResNet50 Convolutional Neural Network. This project was done under the supervision of Professor [Yen Kuang Chen](https://www.linkedin.com/in/ykchen/).

## Methodology
1. **Data Preprocessing:**
   - Standardized images to 224x224 pixels in JPEG format.
   - Utilized OpenCV’s Haar Cascade Classifier for face detection.
   - Cropped and resized detected faces.

2. **Dataset Splitting and Augmentation:**
   - 80/20 split for training and validation datasets.
   - Augmented dataset by horizontally flipping images.

3. **Model Training:**
   - Used pre-trained ResNet50 model.
   - Trained over 10 epochs using Adam Optimizer.

## Dataset Structure

### Original Dataset
The original dataset used in this project was provided by Professor [Yen Kuang Chen](https://www.linkedin.com/in/ykchen/) and cannot be included here.

### How to Structure Your Own Dataset
To replicate the project, you can create your own dataset following these structures:

**Training Dataset:**
```
training/
├── person1/
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
├── person2/
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
└── ...
```

**Testing Dataset:**
```
testing/
├── img1.jpg
├── img2.jpg
├── ...
└── labels.txt (Format: img1.jpg person1, img2.jpg person2, ...)
```

The `labels.txt` file should have each image and its corresponding label on a new line, like this:
```
img1.jpg person1
img2.jpg person2
...
```

The code expects the dataset to be in this format for proper functioning.

## How to Run the Code

1. Follow the Google Colab link: [Face Recognition](https://colab.research.google.com/drive/1O-ZH_ZOsVkYvj72at-WlRFy3_t6EUMOh?usp=sharing)
2. Click on "File" > "Save a copy in Drive" to save a copy of the notebook to your Google Drive.
3. In your Google Drive, create the dataset directories (`training` and `testing`) and upload your images as described in the Dataset Structure section.
4. Update the code in the notebook to point to the correct dataset directories in your Google Drive. For example:
   ```python
   test_folder = '/content/drive/MyDrive/Face-Recognition/testing'
   labels_file = '/content/drive/MyDrive/Face-Recognition/testing/labels.txt'
   ```
5. Run the cells in the notebook to preprocess the data and train the model.

## Note
The original dataset used in this project was provided by Professor [Yen Kuang Chen](https://www.linkedin.com/in/ykchen/) and cannot be included here. However, you can use your own dataset to run the code.

## Files Included
- [notebooks/Face Recognition.ipynb](notebooks/Face%20Recognition.ipynb): The python notebook added to this repository.
- [reports/Project_Report.pdf](reports/Project_Report.pdf): Detailed project report.

## Course Information
- **Course Title:** COEN 240 - Machine Learning
- **Professor:** [Yen Kuang Chen](https://www.linkedin.com/in/ykchen/)