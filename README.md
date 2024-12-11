# IBBNet

**Note:** The full implementation of this method will be uploaded after the complete publication of the related paper.

**Acknowledgment:** This project builds upon the foundational code provided by [https://github.com/jiwoon-ahn/irn](https://github.com/jiwoon-ahn/irn).

## Project Overview
This is a deep learning-based project designed to tackle Weakly Supervised Semantic Segmentation (WSSS) tasks using weak labels such as image-level labels, point labels, bounding box labels, and scribble labels. The project focuses on image-level label-based WSSS, a common approach due to its simplicity and widespread use.

## Features
- Supports WSSS using image-level labels.
- Implements the Iterative Background Blur (IBB) method to improve CAM quality.
- Addresses over-activation and under-activation issues in conventional CAMs by enhancing background and foreground differentiation.
- Employs a novel iterative framework with Grad Fusion Module (GFM) and Partial Reactivation Module (PRM) for generating high-quality pseudo labels.

## Environment Requirements

Ensure your development environment meets the following requirements:

- Python Version: `>=3.x`
- Dependencies:
  - `numpy`
  - `pandas`
  - `torch` or `tensorflow`
  - `matplotlib` or other visualization tools

You can install all dependencies using the following command:

```bash
pip install -r requirements.txt
```

## Usage

### Data Preparation
The datasets used in this project are PASCAL VOC 2012 and COCO. You can download them from the following links:

- PASCAL VOC 2012: [Download Link](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/)
- COCO: [Download Link](https://cocodataset.org/#download)

1. Download or prepare your dataset.
2. Place the data under the `data/` directory or specify the data path in the configuration file.

### Train the Model
Run the following command to start training:

```bash
python train.py --config config.yaml
```

You can modify the `config.yaml` file to adjust training parameters such as learning rate, batch size, etc.

### Evaluate the Model
After training, evaluate the model using the following command:

```bash
python evaluate.py --model_path checkpoints/best_model.pth
```

### Inference Example
Run inference using the following command:

```bash
python infer.py --input input_data_path
```

## Project Structure

```plaintext
├── data/                   # Data directory
├── models/                 # Model definitions
├── checkpoints/            # Saved model weights
├── utils/                  # Utility functions
├── train.py                # Training script
├── evaluate.py             # Evaluation script
├── infer.py                # Inference script
├── config.yaml             # Configuration file
└── requirements.txt        # Dependency list
```


## Contact

If you have any questions while using this project, please contact us via:

- Email: [your-email@example.com](mailto:your-email@example.com)
- GitHub Issues: [Submit an issue](https://github.com/your-repo/issues)

## License

This project is licensed under the [MIT License](LICENSE). You are free to copy, modify, and distribute this code, but you must retain the original copyright notice.
