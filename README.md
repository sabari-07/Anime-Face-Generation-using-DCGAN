# Anime-Face-Generation-using-DCGAN
This project demonstrates how to generate anime faces using a Deep Convolutional Generative Adversarial Network (DCGAN). DCGANs are a type of Generative Adversarial Network (GAN) specifically designed for generating high-quality images. In this project, we apply DCGANs to create anime-style faces.

Table of Contents
Introduction
Dependencies
Dataset
Usage
Model Architecture
Results
License
Contact
Introduction
The goal of this project is to generate anime faces by training a DCGAN on a dataset of anime images. DCGANs use a combination of Convolutional Neural Networks (CNNs) and adversarial training to generate realistic images from random noise. This project showcases how DCGANs can be used to create art-style images, specifically anime faces.

Dependencies
To run this project, you will need the following libraries:

numpy
matplotlib
tensorflow (including keras)
Pillow (PIL)
tqdm
You can install the required libraries using pip:

bash
Copy code
pip install numpy matplotlib tensorflow pillow tqdm
Dataset
This project uses a dataset of anime images. You can use datasets such as Danbooru or Kaggle's Anime Face Dataset.

Download the dataset.
Place the images in a directory named data/anime_faces.
Usage
Clone the Repository

bash
Copy code
git clone https://github.com/sabari-07/anime-face-generation-dcgan.git
cd anime-face-generation-dcgan
Preprocess Data

Preprocess the images to the required size and format. The preprocessing script will resize images and normalize pixel values.

bash
Copy code
python preprocess_data.py --data_dir data/anime_faces
Train the DCGAN

Run the training script to start training the DCGAN model on your dataset. Adjust the hyperparameters as needed.

bash
Copy code
python train_dcgan.py --epochs 50 --batch_size 64
Generate Anime Faces

After training, you can generate new anime faces using the trained model. Specify the number of images you want to generate.

bash
Copy code
python generate_images.py --num_images 10
Generated images will be saved in the generated_images directory.

Model Architecture
Generator: A Convolutional Neural Network that takes random noise as input and generates anime faces. Includes layers such as Conv2DTranspose and BatchNormalization to upscale the input noise.
Discriminator: A Convolutional Neural Network that classifies images as real (from the dataset) or fake (generated by the generator). Includes layers such as Conv2D and LeakyReLU.
Adversarial Training: The generator and discriminator are trained simultaneously, with the generator aiming to create realistic images and the discriminator aiming to distinguish real from fake images.
Results
Examples of generated anime faces can be found in the generated_images directory. The quality of generated images may improve with additional training epochs and hyperparameter tuning.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For any questions or feedback, please contact

GitHub Profile: github.com/sabari-07
