# RPG-StyleGAN

This repo contains a Generative Adversarial Network (GAN) model trained using StyleGAN-ada-2 to generate RPG (Role-Playing Game) sprites. Each sprite consists of four images showing it from different perspectives: front, behind, right, and left. The model was trained on a dataset of 912 sprites styled after old RPG games.

## Model Details
- **Architecture**: StyleGAN-ada-2
- **Training Steps**: Almost 300 epochs
- **FID50k_full Score**: 8.2311772

## Training Set Information
- The training set contains 912 RPG sprites mostly from old games.
- Each image has a shape of `[3, 128, 128]` and are converted to RGB with a resolution of 128x128 pixels.
- Each image consists of 4 aspects of the character(front, rear, right, left).

## Results
Judging by the fid50k_full score, The model has pretty much captured the gist of RPG art style, producing sprites that exhibit the commonly known characteristics of RPG game sprites.

## Usage
To generate RPG sprites using the trained model, follow these steps:
1. Clone the repository.
2. Clone the official repo of [StyleGAN2-ada](https://github.com/NVlabs/stylegan2-ada-pytorch)
3. Install the necessary dependencies(you might need to debug the `conv2d_gradfix.py` and `grid_sample_gradfix.py` yourself to avoid PyTorch version mismatch errors)
4. Run the provided scripts or integrate the model into your project for sprite generation.

## Example Output
Real Sprites:
![Real](https://github.com/Hexanol777/RPG-SpriteGAN/blob/main/results/Real.png)

Synthesized Sprites:
![Synthesized](https://github.com/Hexanol777/RPG-SpriteGAN/blob/main/results/Synthesized.png)


