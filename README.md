
# **Edge-Optimized Deep Learning for Insect Classification**

## Overview

This project focuses on developing edge-optimized deep learning models for classifying agricultural insects. The models are designed to run efficiently on mobile and edge devices, providing farmers with real-time tools to identify and manage harmful crop pests. This work demonstrates the application of **MobileViT** and **EfficientNetV2B2** architectures, optimized using techniques such as **post-training quantization**, **quantization-aware training**, and **representative data quantization**.

The accompanying mobile application integrates these models to deliver an accessible, on-device solution for farmers, ensuring practical applicability in resource-constrained environments.

---

## Features

- **Advanced Architectures**: Leverages MobileViT and EfficientNetV2B2 for high-performance image classification.
- **Optimized for Edge Devices**: Implements TensorFlow Lite for efficient, on-device inference.
- **Custom Dataset**: Uses the *Dangerous Farm Insects Dataset*, consisting of 1,500 images across 15 insect classes.
- **Mobile Application**: A cross-platform app developed using Flutter to enable real-time pest identification.
- **Quantization Techniques**: Detailed trade-offs between model accuracy, size, and inference speed across quantization strategies.

---

## Dataset

The **Dangerous Farm Insects Dataset** includes 1,500 images of pests across 15 classes. Each class represents a specific crop-damaging insect, such as locusts, aphids, and beetles. The dataset emphasizes region-specific and realistic scenarios to aid localized pest management efforts.

---

## Results

### Model Performance

| Model               | Validation Accuracy (%) | Test Accuracy (%) |
|---------------------|-------------------------|-------------------|
| MobileViT           | 82.6                   | 73.4             |
| EfficientNetV2B2    | 80.9                   | 77.8             |

### Quantization Impact

| Model               | Quantization Type       | Model Size (MB) | Test Accuracy (%) | Inference Time (Per Image) |
|---------------------|-------------------------|----------------|-------------------|----------------------------|
| MobileViT           | None                   | 22             | 73.4             | 0.01s                     |
| MobileViT           | Post-Training          | 5.4            | 66.1             | 0.34s                     |
| EfficientNetV2B2    | None                   | 33             | 77.8             | 0.24s                     |
| EfficientNetV2B2    | Post-Training          | 9.6            | 77.8             | 0.20s                     |

---

## Mobile Application

A Flutter-based app integrates the optimized models for on-device classification. Key features include:

- **Real-Time Detection**: Capture or upload insect images for instant classification.
- **Offline Operation**: No internet connection required for inference.
- **Detailed Analysis**: Displays confidence scores and offers mitigation strategies via Firebase integration.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
