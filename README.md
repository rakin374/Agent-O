# Agent-O: Multimodal Skin Cancer Detection

## Project Overview

This project implements a multimodal machine learning approach for skin cancer detection, utilizing both tabular and image data to classify lesions as benign or malignant. The project was developed as part of the CS640 course, combining advanced techniques in data preprocessing, machine learning, and deep learning.


## Team Members

- **Efim**: Methods for Tabular Data
- **Rakin**: Data Analysis, Discussion
- **Kenji**: Methods for Fusion, Conclusion
- **Sam**: Methods for Visual Data/Experiments and Results


## Dataset

The project uses the ISIC (International Skin Imaging Collaboration) dataset for skin lesion classification. The dataset contains medical images and associated metadata for skin cancer detection.


### Dataset Characteristics

- **Initial Class Distribution**:

  - Benign (0): 99.90%
  - Malignant (1): 0.10%

- **Resampled Class Distribution**:

  - Benign (0): 67.10%
  - Malignant (1): 32.90%


## Methodologies

### Tabular Data Processing

- Imported data as a DataFrame
- Dropped rows with null values
- One-hot encoded categorical string columns
- Selected location column with median unique labels


## Model: XGBoost Classifier

- Addressed class imbalance by adjusting dataset
- Achieved high accuracy for both positive and negative cases


### Image Data Processing

## Model: Visual Transformer (ViT)

- Used pre-trained ViT model from 'vit-base-patch16-224-in21k'

- Image preprocessing:

  - Converted byte strings to images
  - Resized to 224x224 pixels

- Data augmentation techniques:

  - Image rotation
  - Recoloring


### Fusion Approach

- XGBoost was utilized for model fusion and final classification


## Experimental Results

### Model Performance

- **Tabular Model**: 97.6% Accuracy
- **Visual Model**: 84.5% Accuracy


### Key Observations

- Tabular model outperformed visual model
- Class imbalance significantly impacted model performance
- Data augmentation slightly improved visual model results


## Key Libraries and Technologies

- PyTorch
- Transformers
- XGBoost
- Scikit-learn
- OpenCV
- Pandas
- Matplotlib
- Seaborn


## Installation

1. Clone the repository

<!---->

    bash
    Copy
    git clone https://github.com/rakin374/Agent-O.git
    cd Agent-O

2. Create a virtual environment

<!---->

    bash
    Copy
    python -m venv venv
    source venv/bin/activate

3. Install dependencies

<!---->

    bash
    Copy
    pip install -r requirements.txt


## Usage

Refer to the Jupyter notebooks in the repository for detailed usage instructions and model training scripts.


## Future Work

- Explore more advanced data augmentation techniques
- Investigate ensemble methods
- Collect more diverse training data
- Improve visual model feature extraction


## Citation

Dosovitskiy, A., et al. "An image is worth 16x16 words: Transformers for image recognition at scale." arXiv preprint arXiv:2010.11929 (2020).


## License

\[Specify License Here]


## Acknowledgments

This project was completed as part of the CS640 course.
