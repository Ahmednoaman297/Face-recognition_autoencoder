# Face Recognition Using Encoder-Decoder Networks

This project aims to create and train an encoder-decoder network for the face recognition problem using datasets such as CASIA WebFace or FRGC. The network is designed, trained, and evaluated using TensorFlow, and different types of autoencoders are implemented and compared.

---

## Table of Contents
1. [Datasets and Preprocessing](#datasets-and-preprocessing)
2. [Model Architectures](#model-architectures)
   - [Vanilla Autoencoder](#vanilla-autoencoder)
   - [Variational Autoencoder (VAE)](#variational-autoencoder-vae)
   - [Convolutional Autoencoder (CAE)](#convolutional-autoencoder-cae)
3. [Cross-Validation](#cross-validation)
4. [Evaluation Metrics](#evaluation-metrics)
5. [Results](#results)
6. [Installation and Usage](#installation-and-usage)
7. [Acknowledgments](#acknowledgments)

---

## Datasets and Preprocessing
1. **Datasets**:
   - CASIA WebFace
   - FRGC

2. **Data Splitting**:
   - 70% for training
   - 15% for validation
   - 15% for testing

3. **Normalization**:
   - Normalize data by subtracting the mean and dividing by the standard deviation for each dimension.
   - Visualizations are provided to verify the effect of normalization.

---

## Model Architectures
Three types of encoder-decoder networks are implemented:

### Vanilla Autoencoder
- A basic autoencoder with fully connected layers.
- Activation: ReLU for hidden layers and sigmoid for the output layer.

### Variational Autoencoder (VAE)
- Encodes input data into a probabilistic latent space.
- Includes reparameterization trick to allow backpropagation.

### Convolutional Autoencoder (CAE)
- Uses convolutional layers for encoding and decoding.
- Captures spatial features more effectively, making it suitable for image data.

---

## Cross-Validation
- **Goal**: Determine the optimal number of hidden layers and nodes per layer.
- **Approach**: Grid search over multiple architectures.

---

## Evaluation Metrics
1. Training loss vs. iterations plot.
2. Recognition accuracy using the minimum Euclidean distance classifier based on feature vectors from the encoder output.

---

## Results
1. **Best Accuracy**:
   - Determined through evaluation on the testing set.
   
2. **Performance Comparison**:
   - Vanilla Autoencoder
   - Variational Autoencoder (VAE)
   - Convolutional Autoencoder (CAE)

3. **Visualization**:
   - Training process (loss vs. iterations).
   - Normalized data.

---

## Installation and Usage

### Prerequisites
1. Python 3.8+
2. TensorFlow 2.8+
3. Additional libraries:
   - NumPy
   - Matplotlib
   - Scikit-learn

### Steps to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<username>/<repo_name>.git
   ```

2. Navigate to the project directory:
   ```bash
   cd <repo_name>
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the training script:
   ```bash
   python train.py
   ```

5. Evaluate the model:
   ```bash
   python evaluate.py
   ```

---

## Acknowledgments
- CASIA WebFace Dataset: [Link](http://www.cbsr.ia.ac.cn/english/CASIA-WebFace-Database.html)
- FRGC Dataset: [Link](https://www.nist.gov/programs-projects/face-recognition-grand-challenge-frgc)
- TensorFlow Documentation: [Link](https://www.tensorflow.org/)

---

This project was developed as part of an academic course assignment. Contributions and improvements are welcome!

