# ☁️ Cloud-based Real-time DGA Detection Engine  
This project provides a **Flask-based web API** for detecting **Domain Generation Algorithm (DGA)** domains in real time using a pre-trained **LSTM model**. The engine classifies incoming domains as either **DGA (malicious/suspicious)** or **Non-DGA (benign)** and can be deployed as a lightweight cloud service.

## 🚀 Features
- LSTM-based sequence model trained to detect DGA vs benign domains  
- Flask REST API for real-time predictions  
- Simple `/` route for health check  
- `/dgaCheck?domain=<your_domain>` endpoint for DGA detection  
- Returns a clear JSON response with classification result  
- Supports real-time classification of domains with a probability score

## 🚧 Tech Stack
- **Backend Framework:** Flask 1.1.1
- **Machine Learning Library:** Keras 2.3.1 with TensorFlow 1.13.2
- **Data Processing:** Pandas 1.0.1 and NumPy 1.18.1
- **Model Serialization:** Pickle
- **Server:** Gunicorn 20.0.4

## 📦 Installation
1. Clone the repository using `git clone https://github.com/your-repo/Cloud-based-Real-time-DGA-Detection-Engine.git`
2. Create a virtual environment using `python -m venv venv`
3. Activate the virtual environment using `source venv/bin/activate` (on Linux/Mac) or `venv\Scripts\activate` (on Windows)
4. Install the required packages using `pip install -r requirements.txt`

## 📈 Usage
1. Start the server using `gunicorn -w 4 app:app`
2. Access the health check endpoint at `http://localhost:5000/`
3. Use the DGA detection endpoint at `http://localhost:5000/dgaCheck?domain=<your_domain>`

## 🗂️ Folder Structure
- `app.py`: The main application file
- `model.pkl`: The pre-trained LSTM model
- `requirements.txt`: The list of required packages
- `Procfile`: The configuration file for the server

## 🤝 Contributing
1. Fork the repository using the GitHub web interface
2. Create a new branch using `git checkout -b your-branch`
3. Make your changes and commit them using `git commit -m "your-commit-message"`
4. Push your changes to your fork using `git push origin your-branch`
5. Create a pull request to merge your changes into the main repository

Please ensure that your contributions follow the existing code style and include any necessary documentation or tests.