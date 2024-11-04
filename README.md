# Myntra Voice Product Recommendation System

## Overview

The Myntra Voice Product Recommendation System is a web application designed to provide product recommendations based on user input, either through voice or text. The system utilizes a combination of natural language processing (NLP) and machine learning techniques to understand user queries and suggest the most similar products from a dataset. The frontend is built with React, and the backend is powered by Flask.

## Features

- **Voice and Text Input**: Users can input their queries via voice or text.
- **BERT-based Recommendations**: Utilizes BERT embeddings for understanding and finding similar products.
- **Product Image Display**: Displays the image of the recommended product.
- **Responsive Design**: Optimized for different screen sizes and devices.
- **CORS Enabled**: Ensures smooth communication between frontend and backend.

## Technologies Used

- **Frontend**: React
- **Backend**: Flask, Flask-CORS
- **NLP Model**: BERT (from Hugging Face's Transformers library)
- **Speech Recognition**: `speech_recognition` library
- **Data Processing**: pandas, numpy
- **Miscellaneous**: pyttsx3, requests, PIL, matplotlib

## Project Structure

```plaintext
Myntra_voice_reccomendation_system/
├── backend/
│   ├── app.py
│   ├── pre_compute_embeddings.py
│   ├── product_embeddings.pkl
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── ProductRecommendation.js
│   │   │   ├── App.js
│   │   ├── App.css
│   │   ├── index.js
│   ├── package.json
├── myenv/
├── README.md
```

## Setup and Installation

### Prerequisites

- Python 3.7 or higher
- Node.js and npm
- Virtual environment tool (e.g., `virtualenv` or `venv`)

### Backend Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-repo/Myntra_voice.git
   cd Myntra_voice/backend
   ```

2. **Create and activate a virtual environment**:
   ```bash
   python -m venv myenv
   myenv\Scripts\activate  # On Windows
   source myenv/bin/activate  # On macOS/Linux
   ```

3. **Install the required packages**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Pre-compute product embeddings**:
   Ensure your `fashion.csv` file is in the backend directory. Then run:
   ```bash
   python pre_compute_embeddings.py
   ```

5. **Run the backend server**:
   ```bash
   python app.py
   ```

### Frontend Setup

1. **Navigate to the frontend directory**:
   ```bash
   cd ../frontend
   ```

2. **Install the required packages**:
   ```bash
   npm install
   ```

3. **Run the frontend server**:
   ```bash
   npm start
   ```

### Verifying Installation

- The Flask backend should be running at `http://localhost:5000`.
- The React frontend should be running at `http://localhost:3000`.

## Usage

1. Open the React application in your web browser.
2. Enter a product-related query using the text input field or use the microphone button to input your query via voice.
3. Click on the "Get Recommendation" button.
4. The recommended product and its image will be displayed below the input field.

## Troubleshooting

### Common Issues

- **ModuleNotFoundError for flask_cors**: Ensure `Flask-Cors` is installed in the virtual environment. Activate the environment and run `pip install flask-cors`.
- **CORS issues**: Ensure CORS is properly configured in the Flask backend using `CORS(app)`.

### Debugging Tips

- Use `console.log` in React and `print` statements in Flask to debug issues.
- Ensure the backend server is running before making requests from the frontend.
- Check browser console and terminal logs for error messages.


## Acknowledgements

- [Hugging Face Transformers](https://github.com/huggingface/transformers)
- [Flask](https://flask.palletsprojects.com/)
- [React](https://reactjs.org/)
- [SpeechRecognition](https://pypi.org/project/SpeechRecognition/)
- [pyttsx3](https://pypi.org/project/pyttsx3/)

---
