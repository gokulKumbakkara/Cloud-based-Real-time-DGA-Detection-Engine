# Cloud-based Real-time DGA Detection Engine

*A Flask-based web API for detecting Domain Generation Algorithm (DGA) domains in real time using a pre-trained LSTM model.*

The engine classifies incoming domains as either **DGA (malicious/suspicious)** or **Non-DGA (benign)** and can be deployed as a lightweight cloud service.

## Features

- LSTM-based sequence model trained to detect DGA vs. benign domains
- Flask REST API for real-time predictions
- Simple `/` route for health check
- `/dgaCheck?domain=<your_domain>` endpoint for DGA detection
- Returns a clear JSON response with the classification result
- Real-time classification of domains with a probability score

## Tech Stack

| Layer | Technology |
|---|---|
| Backend framework | Flask 1.1.1 |
| Machine learning | Keras 2.3.1 with TensorFlow 1.13.2 |
| Data processing | Pandas 1.0.1, NumPy 1.18.1 |
| Model serialization | Pickle |
| WSGI server | Gunicorn 20.0.4 |

## Getting Started

### Prerequisites

- Python 3.x (the pinned dependencies — TensorFlow 1.13.2, Keras 2.3.1 — expect an older Python 3.6/3.7 environment)
- pip

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/gokulKumbakkara/Cloud-based-Real-time-DGA-Detection-Engine.git
   ```
2. Create a virtual environment:
   ```bash
   python -m venv venv
   ```
3. Activate the virtual environment:
   ```bash
   source venv/bin/activate   # Linux/Mac
   venv\Scripts\activate      # Windows
   ```
4. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Start the server:
   ```bash
   gunicorn -w 4 app:app
   ```
2. Access the health check endpoint at `http://localhost:5000/`
3. Use the DGA detection endpoint at `http://localhost:5000/dgaCheck?domain=<your_domain>`

## Contributing

1. Fork the repository using the GitHub web interface
2. Create a new branch using `git checkout -b your-branch`
3. Make your changes and commit them using `git commit -m "your-commit-message"`
4. Push your changes to your fork using `git push origin your-branch`
5. Create a pull request to merge your changes into the main repository

Please ensure that your contributions follow the existing code style and include any necessary documentation or tests.
