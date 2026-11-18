ISL to Audio – Indian Sign Language Translator

An AI-powered application that recognizes Indian Sign Language (ISL) alphabet hand gestures through a webcam and converts them into spoken audio. This project aims to reduce communication barriers between ISL users and people who do not understand sign language.

1. Problem Statement

Many deaf and hard-of-hearing individuals use Indian Sign Language as their primary means of communication. However, limited awareness of sign language creates communication barriers in everyday situations.

This project aims to bridge this gap using computer vision and machine learning to recognize ISL alphabet gestures and convert recognized words into speech.

2. Current Status – TRL 2

Current Technology Readiness Level: TRL 2 – Technology Concept Formulated

The project has reached the following development milestones:

- Collected a custom dataset covering 26 English alphabets using ISL hand signs.
- Developed and trained a Random Forest machine learning model.
- Reported 99.75% accuracy on the current held-out recording test.
- Implemented real-time webcam-based hand gesture recognition.
- Integrated text-to-speech conversion using pyttsx3.
- Implemented continuous letter recognition and automatic word formation.
- Developed pause-based word completion and automatic speech output.

Testing note: The reported accuracy is based on the current dataset and testing conditions. Further independent testing with different users and environments is required.

3. How It Works

1. Image Acquisition: A webcam captures hand gestures in real time.
2. Hand Detection: MediaPipe detects the hand and extracts 21 hand landmarks.
3. Feature Extraction: Landmark coordinates are normalized and converted into numerical features.
4. Alphabet Classification: A Random Forest model predicts the corresponding alphabet.
5. Word Formation: Recognized letters are combined to form words.
6. Speech Generation: Completed words are converted into spoken audio using pyttsx3.

4. Technology Stack

Technology| Purpose
Python 3.12| Programming language
OpenCV| Computer vision
MediaPipe| Hand landmark detection
Scikit-learn| Random Forest classification
NumPy| Numerical processing
Pandas| Dataset management
Joblib| Model storage
pyttsx3| Text-to-speech conversion
Webcam| Real-time image capture

5. Project Structure

ISL-to-Audio/
│
├── dataset/
│   └── alphabet/
│       └── alphabet_landmarks.csv
│
├── models/
│   └── alphabet_model.joblib
│
├── collect_alphabet.py
├── check_dataset.py
├── train_alphabet.py
├── live_alphabet.py
├── live_alphabet_v2.py
│
├── requirements.txt
├── .gitignore
├── LICENSE
└── README.md

6. How to Run

Prerequisites

- Python 3.12
- Laptop or desktop with a webcam
- Required Python libraries

Step 1: Clone the Repository

git clone YOUR_REPOSITORY_URL
cd ISL-to-Audio

Replace "YOUR_REPOSITORY_URL" with the actual GitHub repository URL.

Step 2: Create a Virtual Environment

python -m venv venv

Step 3: Activate the Environment (Windows)

venv\Scripts\activate

Step 4: Install Dependencies

pip install -r requirements.txt

Step 5: Run the Application

python live_alphabet_v2.py

Note: The trained model and dataset must be available in their respective folders. If the model is not included, generate it by running the dataset preparation and training scripts.

7. Project Roadmap

- [x] Collect a custom dataset for ISL alphabets A–Z.
- [x] Train the alphabet recognition model.
- [x] Implement real-time hand gesture recognition.
- [x] Integrate text-to-speech conversion.
- [x] Implement continuous letter recognition.
- [x] Develop automatic word formation.
- [x] Implement pause-based word completion.
- [ ] Improve recognition reliability across different users.
- [ ] Expand recognition to common ISL words and phrases.
- [ ] Develop sentence-level translation.
- [ ] Prepare a technical report and demonstration video.
- [ ] Conduct testing with ISL users.

8. Future Scope

- Recognition of dynamic ISL gestures and commonly used words.
- Sentence-level translation with appropriate ISL grammar considerations.
- Improved recognition under different lighting conditions and backgrounds.
- Development of a portable sign-language translation system.
- Exploration of wearable technology for real-time communication.

9. Author

Sheik Abdullah M
Mechanical Engineering
KPR Institute of Engineering and Technology
Coimbatore, Tamil Nadu, India
