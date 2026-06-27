# Deepfake-Image-Detection-Using-Machine-Learning-
I built a DeepFake detection system that uses Convolutional Neural Networks to classify facial image inputs as real or fake. The model was trained on thousands of labeled images and can make predictions through a graphical user interface.

# Deepfake Image Detection Using Machine Learning

A robust, full-stack Deepfake Image Detection system that utilizes custom Convolutional Neural Networks (CNN) implemented in PyTorch to classify facial image inputs as either real or fake. The project features an integrated backend deployment using Flask, allowing users to upload images and receive instant diagnostic predictions through an interactive graphical user interface.

---

## 📂 Repository Structure

The repository is structured to maintain a clean separation between application source code, model artifacts, and repository configuration:

```text
Deepfake-Image-Detection-Using-Machine-Learning--main/
│
├── app.py                      # Main Flask application (Routing & Web Interface)
├── deepfake_detection_dual.py  # Model inference script & pipeline configuration
├── deepfake_pytorch_model.pth  # Trained PyTorch CNN weights artifact
├── LICENSE                     # Apache-2.0 open-source license
└── README.md                   # Project documentation
🛠️ Technical Architecture & Core Pillars
1. Deep Learning Inference Pipeline (PyTorch)
The core detection engine is powered by a Convolutional Neural Network (CNN) designed to capture subtle frequency anomalies, blending artifacts, and inconsistent patterns typical of AI-generated deepfakes.

Preprocessing Engine: Standardizes incoming web uploads via automated resizing, normalization matching the training distribution, and tensor conversion.

Model Weights (.pth): Loaded efficiently during backend initialization to execute high-speed forward passes for classification.

2. Full-Stack Web Controller (Flask)
Model-View-Controller Pattern: app.py serves as the primary controller, exposing secure API endpoints to receive user image file streams via POST requests.

Real-time Diagnostics: Binds the asynchronous processing pipeline to the graphical user interface, rendering prediction classes (Real/Fake) along with corresponding confidence metrics instantly.

📊 System Execution Lifecycle
Plaintext
 [User Interface]          [Flask Backend (app.py)]       [Inference Engine]
        │                             │                            │
        ├─── 1. Upload Image ────────>│                            │
        │    (via Web GUI)            ├─── 2. Preprocess Tensor ──>│
        │                             │    (Resize & Normalize)    │
        │                             │                            │
        │                             │<── 3. Execute CNN Model ───┤
        │                             │    (Compute Logits)        │
        │<── 4. Render Results ───────┤                            │
        │    (Prediction Class)       │                            │
🚀 Step-by-Step Local Setup & Execution
Prerequisites
Ensure you have Python 3.8+ installed on your system.

1. Clone the Repository
Bash
git clone [https://github.com/Pruthviraj-01/Deepfake-Image-Detection-Using-Machine-Learning--main.git](https://github.com/Pruthviraj-01/Deepfake-Image-Detection-Using-Machine-Learning--main.git)
cd Deepfake-Image-Detection-Using-Machine-Learning--main
2. Create and Activate a Virtual Environment
Bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/macOS
python3 -m venv venv
source venv/bin/activate
3. Install Dependencies
Install the required core machine learning and web dependencies:

Bash
pip install torch torchvision flask Werkzeug Pillow numpy
4. Run the Application
Launch the local development web server:

Bash
python app.py
Open your browser and navigate to http://127.0.0.1:5000/ to interact with the GUI.

🔒 Security & Optimization Considerations
Secure File Handling: Utilizes safe filename parsing utilities via Werkzeug to prevent directory traversal vulnerabilities during web image uploads.

Memory Efficiency: The model executes prediction cycles within an explicit inference context (torch.no_grad()), preventing gradient calculation graphs from consuming unnecessary system memory resources.

📄 License
This project is open-source and licensed under the terms of the Apache-2.0 License.
