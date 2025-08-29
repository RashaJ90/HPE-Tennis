# Pose2Trajectory: Predicting Tennis Player Trajectory with Transformers

This project, `HPE-Tennis`, is an implementation of the concepts presented in the paper **"Pose2Trajectory: Using Transformers on Body Pose to Predict Tennis Player’s Trajectory"**. It aims to predict the future trajectory of a tennis player based on their body joint data and the ball's position using a Transformer-based architecture, enhanced with Generative Adversarial Networks (GANs) for realistic motion visualization.

This can be used to assist camera operators in production by enabling cameras to automatically track players without human intervention.

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Project Overview

The core idea of this project is to predict tennis player movements and generate realistic visualizations of future poses. Traditional methods often rely on centroid tracking, but this project takes a more granular approach by using human body pose information combined with generative modeling for motion prediction and visualization.

## Key Features

- **Player Detection**: Detects tennis players in video frames.
- **Ball Detection**: Detects the tennis ball's position, a critical component for predicting player movement.
- **Human Pose Estimation**: Extracts key body joints of the player.
- **Trajectory Prediction**: Employs a Transformer network to process the sequence of poses and ball positions.
- **Motion Forecasting**: Predicts future player poses and movements using temporal sequence modeling.
- **Realistic Visualization**: Generates photorealistic images of predicted player movements using conditional GANs.


## Model Architecture

The prediction system consists of three main components:

### 1. Pose Prediction Pipeline
- **Encoder**: Processes the input sequence of player body joints and ball positions to create a rich contextual representation.
- **Decoder**: Takes the encoder's output and autoregressively generates the future trajectory of the player's centroid coordinates.

### 2. Motion Forecasting Module
- **Temporal Transformer**: Predicts future joint positions based on historical pose sequences.
- **Spatio-temporal Modeling**: Captures both spatial joint relationships and temporal movement patterns.

### 3. Generative Visualization Component
- **Conditional GAN**: Generates realistic tennis player images showing predicted future poses.
- **Pose-to-Image Translation**: Converts predicted joint coordinates into photorealistic player visualizations.
- **Context-Aware Generation**: Incorporates court background and player appearance consistency.

## Installation

To get started with this project, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/HPE-Tennis.git
    cd HPE-Tennis
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements/requirements.txt
    ```

## Usage

Once the installation is complete, you can use the scripts to train the model or run predictions.

### Training

To train the model on the dataset, run the `train.py` script. Make sure your dataset is correctly placed in the `data/` directory.

```bash
python train.py --config configs/training_config.json
```
*(Note: Command is a placeholder and will be updated as the project develops.)*

### Prediction

To predict player trajectories from a video or data file, use the `predict.py` script.

```bash
python predict.py --model_path models/pose2trajectory.pt --input_image path/to/image.png --generate_motion
```
*(Note: Command is a placeholder and will be updated as the project develops.)*

## Dataset

## Results

## Contributing

## License

## Acknowledgments
