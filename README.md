# ppu-yolo-onnx-inference

![YOLOv11 Object Detection](https://img.shields.io/badge/Download%20Latest%20Release-Click%20Here-brightgreen?style=flat-square&logo=github)  
[Download Latest Release](https://github.com/Fayzan6717/ppu-yolo-onnx-inference/releases)

Welcome to the **ppu-yolo-onnx-inference** repository! This project allows you to run YOLOv11 object detection models seamlessly in a TypeScript Bun environment. Say goodbye to the complexities of Python, PyTorch, and heavy dependencies. Here, we focus on making object detection simple and efficient.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- **Lightweight**: No need for Python or PyTorch.
- **TypeScript Compatible**: Works perfectly in a Bun environment.
- **Easy to Use**: Simple API for running object detection.
- **Fast Inference**: Leverage ONNX Runtime for efficient model execution.
- **Supports YOLOv11**: State-of-the-art object detection capabilities.

## Getting Started

To get started with this repository, follow the instructions below. You will set up your environment and run your first YOLOv11 inference.

### Prerequisites

Ensure you have the following installed:

- **Bun**: This project is built for Bun, a fast JavaScript runtime. You can install it from [Bun's official website](https://bun.sh/).
- **Node.js**: While Bun is preferred, having Node.js can help with compatibility.

### Installation

To install the necessary dependencies, clone the repository and install packages:

```bash
git clone https://github.com/Fayzan6717/ppu-yolo-onnx-inference.git
cd ppu-yolo-onnx-inference
bun install
```

### Download the Model

You can download the YOLOv11 ONNX model from the [Releases section](https://github.com/Fayzan6717/ppu-yolo-onnx-inference/releases). Make sure to follow the instructions provided in that section to download and execute the model correctly.

## Usage

Once you have installed the dependencies and downloaded the model, you can start using the library.

### Running Inference

Here's a simple example of how to run object detection using the provided library:

```typescript
import { YOLO } from 'ppu-yolo-onnx-inference';

// Load the model
const model = new YOLO('path/to/your/model.onnx');

// Run inference on an image
const results = await model.detect('path/to/your/image.jpg');

// Display results
console.log(results);
```

### Input Format

The input image should be in a standard format like JPEG or PNG. Ensure the image path is correct to avoid errors.

### Output Format

The output will be an array of detected objects, each containing:

- **Label**: The class of the detected object.
- **Confidence**: The confidence score of the detection.
- **Bounding Box**: The coordinates of the bounding box around the detected object.

## Examples

To help you understand how to use the library effectively, we provide a few examples:

### Example 1: Basic Detection

```typescript
const model = new YOLO('path/to/your/model.onnx');
const results = await model.detect('path/to/your/image.jpg');

results.forEach((result) => {
  console.log(`Detected: ${result.label} with confidence: ${result.confidence}`);
});
```

### Example 2: Handling Multiple Images

You can also run inference on multiple images in a loop:

```typescript
const images = ['image1.jpg', 'image2.jpg', 'image3.jpg'];

for (const image of images) {
  const results = await model.detect(image);
  console.log(`Results for ${image}:`, results);
}
```

## Contributing

We welcome contributions! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Commit your changes with clear messages.
5. Push to your forked repository.
6. Create a pull request.

Please ensure that your code follows the project's coding style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or feedback, feel free to reach out:

- **GitHub**: [Fayzan6717](https://github.com/Fayzan6717)
- **Email**: fayzan@example.com

Thank you for your interest in the **ppu-yolo-onnx-inference** project! We hope you find it useful for your object detection needs. Don't forget to check the [Releases section](https://github.com/Fayzan6717/ppu-yolo-onnx-inference/releases) for the latest updates and models.