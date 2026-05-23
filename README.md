# Object Detection for Autonomous Vehicle Models

A comprehensive repository containing object detection models tailored for autonomous vehicle applications, including state-of-the-art (SOTA) models trained on multiple datasets and custom architectures.

## 📋 Table of Contents

- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Datasets](#datasets)
- [Models](#models)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This repository contains a collection of object detection models specifically optimized for autonomous vehicle perception systems. The models are trained on industry-standard datasets (BDD100K, IDD) and include custom-trained state-of-the-art architectures designed for real-time performance and high accuracy in diverse driving conditions.

### Key Features

- **Multi-Dataset Training**: Models trained on BDD (Berkeley DeepDrive) and IDD (India Driving Dataset)
- **SOTA Architectures**: Custom implementations of modern object detection frameworks
- **Autonomous Vehicle Optimized**: Designed for real-world driving scenarios
- **Production Ready**: Models optimized for deployment in autonomous systems

## 📁 Repository Structure

```
Obj_Det_AV_Models/
├── BDD Models/                          # Models trained on BDD100K dataset
│   └── [BDD-specific model variants]
├── IDD Models/                          # Models trained on IDD dataset
│   └── [IDD-specific model variants]
├── Custom Trained SOTA Models/          # Custom trained state-of-the-art models
│   └── [Latest SOTA implementations]
└── README.md                            # This file
```

### Directory Details

- **BDD Models**: Contains object detection models trained on the Berkeley DeepDrive dataset, featuring diverse driving scenarios across weather conditions and times of day
- **IDD Models**: Models trained on the India Driving Dataset, specialized for challenging unstructured traffic environments
- **Custom Trained SOTA Models**: Latest state-of-the-art models with custom training pipelines and optimizations

## 📊 Datasets

### Berkeley DeepDrive (BDD100K)
- **Coverage**: Diverse driving scenarios including different weather, times of day, and road types
- **Use Case**: General autonomous vehicle perception in varied conditions

### India Driving Dataset (IDD)
- **Coverage**: Unstructured traffic environments typical of developing markets
- **Use Case**: Robust detection in challenging, dense traffic scenarios

## 🤖 Models

This repository includes models for:

- **Vehicle Detection**: Cars, trucks, buses, and other vehicles
- **Pedestrian Detection**: Pedestrians and cyclists
- **Traffic Sign Detection**: Road signs and traffic signals
- **Road Infrastructure**: Lane markings and road boundaries

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- PyTorch or TensorFlow (depending on model)
- OpenCV
- NumPy
- Matplotlib

### Installation

```bash
git clone https://github.com/sarveshvengurlekar/Obj_Det_AV_Models.git
cd Obj_Det_AV_Models
pip install -r requirements.txt
```

## 💻 Usage

### Basic Inference

```python
# Load a model and run inference on an image
from models import load_model

# Load model
model = load_model('path/to/model')

# Run inference
detections = model.predict('path/to/image.jpg')

# Visualize results
model.visualize(detections, 'output.jpg')
```

### Training Custom Models

```bash
python train.py --model <model_name> \
                 --dataset <dataset_path> \
                 --epochs 100 \
                 --batch-size 32
```

### Evaluation

```bash
python evaluate.py --model <model_path> \
                   --dataset <dataset_path> \
                   --metrics mAP,precision,recall
```

## 🔧 Model Details

Each model directory contains:

- **Model weights**: Pre-trained model files
- **Configuration files**: Model architecture and hyperparameters
- **Training logs**: Performance metrics and training history
- **Documentation**: Model-specific usage and performance notes

## 📈 Performance Metrics

Models are evaluated using:

- **mAP (mean Average Precision)**: Primary metric for object detection quality
- **Precision & Recall**: Per-class performance metrics
- **Inference Time**: FPS (frames per second) on standard hardware
- **Robustness**: Performance across different conditions and weather

## 🤝 Contributing

Contributions are welcome! Please feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source. Please see the LICENSE file for details.

## 📧 Contact

For questions or suggestions, please reach out to the repository owner or open an issue.

## 🙏 Acknowledgments

- Berkeley DeepDrive for the BDD100K dataset
- India Driving Dataset creators for the IDD dataset
- The autonomous vehicle research community for advances in object detection

---

**Note**: This repository is under active development. Check back regularly for updates and new models!
