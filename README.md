# DeepFake Image Detector 🔍

A deep learning-based application for detecting deepfake images created with modern AI technologies. This project uses a Convolutional Neural Network (CNN) trained on a comprehensive dataset of real and deepfake images, and provides an interactive web interface powered by Streamlit.

## 📋 Table of Contents

- [Features](#features)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [How It Works](#how-it-works)
- [Future Improvements](#future-improvements)
- [License](#license)
- [Contributing](#contributing)

## ✨ Features

- **Deep Learning Model**: CNN-based architecture with 9 convolutional layers and 3 fully connected dense layers
- **Web Interface**: User-friendly Streamlit web application for easy image upload and analysis
- **Real-time Detection**: Quick prediction results with confidence scores
- **Multiple Format Support**: Supports JPG, JPEG, PNG, and WEBP image formats
- **Pre-trained Model**: Includes a trained model ready for inference

## 🏗️ Model Architecture

The model consists of:
- **Input Layer**: Images resized to 128×128 pixels
- **Convolutional Blocks**: 9 Conv2D layers with increasing filter sizes (32, 64, 128, 256)
- **Pooling Layers**: MaxPooling layers for dimensionality reduction
- **Dense Layers**: 3 fully connected layers (256, 512, 1 neurons)
- **Output**: Binary classification (Real/Fake) with probability scores

## 📊 Dataset

The model was trained on the [Deepfake and Real Images Dataset](https://www.kaggle.com/datasets/manjilkarki/deepfake-and-real-images) from Kaggle, which contains:
- Training set: 140,002 images
- Validation set: 10,905 images
- Test set: 39,428 images

All images are categorized into two classes: Real and Fake (Deepfake).

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Step-by-step Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/deepFake-image-detector.git
   cd deepFake-image-detector
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Verify the model file exists**
   Ensure that `deepfakeImg_detector_1.keras` is present in the project directory.

## 💻 Usage

### Running the Web Application

1. **Start the Streamlit app**
   ```bash
   streamlit run main.py
   ```

2. **Access the application**
   - The app will automatically open in your default web browser
   - If not, navigate to `http://localhost:8501`

3. **Using the Application**
   - Click on "Choose an image..." to upload an image file
   - Supported formats: JPG, JPEG, PNG, WEBP
   - Click the "Predict" button to analyze the image
   - View the prediction result with confidence percentage

### Example Workflow

```
Upload Image → Click Predict → View Results
                         ↓
              "95.23% chances of being Real"
```

## 📁 Project Structure

```
deepFake-image-detector/
│
├── main.py                          # Streamlit web application
├── deepfakeImg_detector.ipynb       # Jupyter notebook for model training
├── deepfakeImg_detector_1.keras     # Pre-trained model file
├── deepfakeImg_detector.keras       # Alternative model file
├── requirements.txt                 # Python dependencies
├── LICENSE                          # Apache License 2.0
└── README.md                        # This file
```

## 📦 Requirements

Key dependencies include:
- **TensorFlow** (2.17.0): Deep learning framework
- **Keras** (3.6.0): High-level neural networks API
- **Streamlit** (1.39.0): Web application framework
- **NumPy** (1.26.4): Numerical computing
- **Pillow** (10.4.0): Image processing

For the complete list, see `requirements.txt`.

## 🔬 How It Works

1. **Image Preprocessing**
   - Image is loaded and resized to 128×128 pixels
   - Pixel values are normalized to the range [0, 1]
   - Image is converted to a NumPy array with batch dimension

2. **Model Inference**
   - Preprocessed image is fed into the trained CNN model
   - Model extracts features through convolutional layers
   - Final dense layer outputs a probability score

3. **Prediction Interpretation**
   - Probability > 0.5: Classified as "Real"
   - Probability ≤ 0.5: Classified as "Fake"
   - Confidence score is displayed as a percentage

## 🔮 Future Improvements

- [ ] Add support for batch image processing
- [ ] Implement video deepfake detection
- [ ] Add visualization of model's attention regions
- [ ] Improve model accuracy with data augmentation techniques
- [ ] Add API endpoint for programmatic access
- [ ] Implement confidence threshold adjustment
- [ ] Add model performance metrics and evaluation results
- [ ] Support for higher resolution images

## 📝 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Contribution Guidelines

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## ⚠️ Important Notes

- This model is trained on a specific dataset and may not generalize perfectly to all types of deepfakes
- Detection accuracy may vary depending on image quality and deepfake generation methods
- The model is intended for research and educational purposes
- Always verify critical decisions with additional verification methods

## 📧 Contact

For questions, issues, or suggestions, please open an issue on GitHub.

---

**Disclaimer**: This tool is provided for educational and research purposes. Deepfake technology is rapidly evolving, and no detection system can guarantee 100% accuracy. Use responsibly and verify critical information through multiple sources.
```

## Improvements

1. Structure: table of contents and clear sections
2. Features: highlights of the app
3. Model details: architecture description
4. Dataset: source and statistics
5. Installation: step-by-step with virtual env
6. Usage: instructions for running the app
7. Project structure: file overview
8. How it works: workflow explanation
9. Future improvements: roadmap
10. Contributing: guidelines
11. Important notes: disclaimers

I can customize any section or add more detail. Switch to agent mode to apply these changes automatically.
