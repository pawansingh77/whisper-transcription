Speech-to-Text Transcription using OpenAI Whisper
This project implements automatic speech recognition (ASR) using OpenAI's Whisper model. It supports two transcription modes:

Dataset-based Transcription: Transcribes audio samples from a dataset.

YouTube-based Transcription: Downloads a YouTube video’s audio and transcribes it.

Installation
Ensure you have Python installed (version 3.8 or later).
Then, install the required dependencies:

pip install torch transformers datasets yt-dlp ffmpeg-python pydub
Additionally, install FFmpeg (required for audio processing):

Linux/macOS:
sudo apt install ffmpeg
Windows: Download from FFmpeg Official Site and add it to system PATH.

Usage
1️⃣ Dataset-Based Transcription
To transcribe pre-existing datasets, run:

python dataset_transcribe.py
This script loads a sample dataset and runs speech-to-text transcription using OpenAI Whisper.

2️⃣ YouTube Video Transcription
To transcribe a YouTube video, run:


python youtube_transcribe.py
This script:

Downloads the audio from a given YouTube link.

Converts the audio to WAV format.

Splits long audio files into 30-second chunks (if needed).

Transcribes speech using OpenAI Whisper.

🔹 To change the YouTube video link, modify video_url inside youtube_transcribe.py.

File Structure

📂 Speech-to-Text-Whisper
│── dataset_transcribe.py      # Script to transcribe dataset audio
│── youtube_transcribe.py      # Script to transcribe YouTube audio
│── README.md                  # Project documentation
│── requirements.txt           # Required dependencies

To install all dependencies at once, run:

pip install -r requirements.txt
