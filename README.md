# 🎶 Music Genre Classifier

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://musicclasifier.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg?style=for-the-badge&logo=python)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00.svg?style=for-the-badge&logo=tensorflow)](https://www.tensorflow.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-Audio-EE4C2C.svg?style=for-the-badge&logo=pytorch)](https://pytorch.org/)

Welcome to the Music Genre Classifier! This AI-powered application is designed to classify music into genres using deep learning. Whether you're a music lover, DJ, or just curious, this tool offers a unique way to explore and analyze your music collection.

---

## 📸 Showcase

| Main Page | How It Works |
| :---: | :---: |
| <img width="500" alt="Main Page" src="https://github.com/user-attachments/assets/34e7095f-3a36-47e9-b49c-00f9da1621f8"> | <img width="500" alt="How It Works" src="https://github.com/user-attachments/assets/b0e53031-710f-45eb-9bba-d89efcc1c97d"> |
| **Prediction in Action** | **Genre Pie Chart** |
| <img width="500" alt="Prediction" src="https://github.com/user-attachments/assets/17c8c72d-b4bc-40fb-b540-0a7427cf1d98"> | <img width="500" alt="Pie Chart" src="https://github.com/user-attachments/assets/e0e4cd51-7f2a-4ea4-b2b6-9a36a8883df7"> |

---

## ✨ Features

- **AI-Powered Classification**: Classifies music into genres using a pre-trained deep learning model.
- **Fast & Easy**: Just upload an audio file, and the app predicts the genre within seconds.
- **Interactive Visualization**: Displays a dynamic pie chart from Plotly showing the genre composition of the audio.
- **User-Friendly Interface**: Built with Streamlit for an interactive and intuitive experience.

---

## 🛠️ Tech Stack

- **Frontend**: Streamlit
- **Deep Learning**: TensorFlow / Keras
- **Audio Processing**: PyTorch / Torchaudio, Librosa
- **Data & Visualization**: NumPy, Plotly

---

## 🚀 Getting Started

To run this application locally, please follow the instructions below.

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/ACHYUTAM2004/Music-genre-clasifier.git](https://github.com/ACHYUTAM2004/Music-genre-clasifier.git)
    cd Music-genre-clasifier
    ```

2.  **Install Dependencies:**
    Ensure you have Python installed. Then, install the required libraries from the `requirements.txt` file.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Download the Pre-trained Model:**
    The model is hosted on Google Drive. Please [download the `Trained_model_final.h5` file from this link](https://drive.google.com/file/d/1zH-zgsuZQU9jverJg5us5w_2YvCJOIO0/view?usp=sharing) and place it in the root directory of the project.

4.  **Run the Application:**
    ```bash
    streamlit run app.py
    ```

---

## 📝 How to Use

1.  **Launch the App**: Run `streamlit run app.py` in your terminal or visit the [live Streamlit app](https://musicclasifier.streamlit.app/).
2.  **Navigate**: Use the sidebar to choose between "About App," "How it Works?," or "Predict Music Genre."
3.  **Upload Audio**: In the prediction section, select an `.mp3` or `.wav` file and upload it.
4.  **Predict Genre**: Click the "Know Genre" button to classify the audio. The app will display a pie chart with the genre predictions.

---

## 🔬 How It Works

This classifier leverages deep learning and digital signal processing to analyze audio and predict genres.

1.  **Audio Processing:** The uploaded audio file is divided into overlapping chunks to capture various sections of the song.
2.  **Feature Extraction:** Each audio chunk is converted into a **Mel Spectrogram** using `torchaudio`. The spectrogram is resized to a (210, 210) format to match the input dimensions expected by the model.
3.  **Model Prediction**: The pre-trained TensorFlow model classifies each chunk into a genre. The final genre is determined by the most frequent prediction across all chunks.
4.  **Visualization**: A Plotly pie chart displays the genre distribution, with the primary genre highlighted.
