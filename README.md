# Deepfake-Image-Detection-Using-Machine-Learning-
I built a DeepFake detection system that uses Convolutional Neural Networks to classify facial image inputs as real or fake. The model was trained on thousands of labeled images and can make predictions through a graphical user interface.

# Deepfake Image Detection Using Machine Learning

A full-stack web application that uses a Convolutional Neural Network (CNN) built with PyTorch to detect deepfake images. The project features a user-friendly web interface powered by Flask where users can upload facial images and receive instant real or fake classifications.

---

<img width="313" height="113" alt="image" src="https://github.com/user-attachments/assets/31775992-a00d-42b2-a1ab-f218cd93c4ce" />

---

## 🛠️ Technical Architecture & Core Pillars

1. Deep Learning Inference Pipeline (PyTorch)
The core detection engine is powered by a Convolutional Neural Network (CNN) designed to capture subtle frequency anomalies, blending artifacts, and inconsistent patterns typical of AI-generated deepfakes.

Preprocessing Engine: Standardizes incoming web uploads via automated resizing, normalization matching the training distribution, and tensor conversion.

Model Weights (.pth): Loaded efficiently during backend initialization to execute high-speed forward passes for classification.

2. Full-Stack Web Controller (Flask)
Model-View-Controller Pattern: app.py serves as the primary controller, exposing secure API endpoints to receive user image file streams via POST requests.

Real-time Diagnostics: Binds the asynchronous processing pipeline to the graphical user interface, rendering prediction classes (Real/Fake) along with corresponding confidence metrics instantly.

---

## 📊 System Execution Lifecycle

<img width="377" height="167" alt="image" src="https://github.com/user-attachments/assets/efd94d74-7822-4b44-8875-5f7b380989b8" />

---

## 🚀 Step-by-Step Local Setup & Execution

Prerequisites
Ensure you have Python 3.8+ installed on your system.

---

1. Clone the Repository - 
git clone [https://github.com/Pruthviraj-01/Deepfake-Image-Detection-Using-Machine-Learning--main.git](https://github.com/Pruthviraj-01/Deepfake-Image-Detection-Using-Machine-Learning--main.git)
cd Deepfake-Image-Detection-Using-Machine-Learning--main

---

2. Create and Activate a Virtual Environment -
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/macOS
python3 -m venv venv
source venv/bin/activate 

---

3. Install Dependencies
Install the required core machine learning and web dependencies:

pip install torch torchvision flask Werkzeug Pillow numpy

---

4. Run the Application
Launch the local development web server:
python app.py
Open your browser and navigate to http://127.0.0.1:5000/ to interact with the GUI.

--- 

## 🔒 Security & Optimization Considerations
Secure File Handling: Utilizes safe filename parsing utilities via Werkzeug to prevent directory traversal vulnerabilities during web image uploads.

Memory Efficiency: The model executes prediction cycles within an explicit inference context (torch.no_grad()), preventing gradient calculation graphs from consuming unnecessary system memory resources.

---
## 📄 License
This project is open-source and licensed under the terms of the Apache-2.0 License. 

--- 

---

## 📌 Conclusion & Future Scope
The successful deployment of this Deepfake Detection system showcases the strength of combining Convolutional Neural Networks with lightweight web frameworks. 

Moving forward, the project can be enhanced by:
* Integrating hybrid architectures (like Vision Transformers) for higher accuracy.
* Adding support for video deepfake analysis frame-by-frame.
* Implementing a confidence percentage score alongside the final classification. 
