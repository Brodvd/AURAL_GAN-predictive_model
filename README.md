# AURAL_GAN+predictive_model

(Discord[https://discord.gg/EQDvjGT7])


This project aims to transform low-quality phone recordings into professional-quality audio using a Generative Adversarial Network (GAN). The system is designed to work with acoustic guitar recordings, but it can be adapted to work with other instruments.

The system works in two main stages:
1. **Training:** In this stage, the system is trained on a dataset of high-quality and low-quality audio files. It learns to transform low-quality audio into high-quality audio by minimizing the difference between the transformed audio and the original high-quality audio. The system uses a GAN architecture, which consists of two neural networks, the Generator and the Discriminator, competing against each other. The Generator tries to create high-quality audio from low-quality input, while the Discriminator tries to distinguish between real high-quality audio and the audio produced by the Generator.
2. **Prediction:** In this stage, the system takes a low-quality audio file as input and transforms it into a high-quality audio file. This process is accomplished by running the low-quality audio through the trained Generator network.

The project includes four main components:
- `main.py`: This is the main script that orchestrates the training and prediction processes. It loads the data, trains the GAN, and performs prediction.
- `data_loader.py`: This script is responsible for loading the audio data, converting it into spectrograms, and preparing it for training. It uses the Librosa library for audio processing.
- `generator.py`: This script defines the Generator part of the GAN, which transforms low-quality audio into high-quality audio. It uses a U-Net architecture, which is a type of Convolutional Neural Network (CNN) that is often used for image and audio enhancement tasks.
- `discriminator.py`: This script defines the Discriminator part of the GAN, which assesses the quality of the audio generated by the Generator. It also uses a CNN architecture.

## Installation

1. Clone this repository to your local machine.
2. Install the required packages using pip:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

To use the system, you need to have a dataset of high-quality and low-quality audio files. These files should be placed in the `acoustic_guitar/high_quality` and `acoustic_guitar/low_quality` directories, respectively.

Once the data is in place, you can train the system by running the main script:

```bash
python src/main.py




