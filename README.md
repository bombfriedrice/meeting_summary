# Meeting Note Generator

This project allows you to transcribe and summarize meetings by recording audio using BlackHole, converting it to text, and then summarizing it using OpenAI's GPT-4.

## Features

- **Transcription**: Convert audio files to text using OpenAI's Whisper model.
- **Summary**: Generate summaries of the transcribed text using GPT-4.
- **Download Options**: Download the transcription and summary in text and DOCX formats.

## Prerequisites

- Python 3.8+
- Streamlit
- OpenAI Python client library
- pydub
- docx
- BlackHole (for capturing system and microphone audio)

## Installation

1. **Clone the Repository**

git clone https://github.com/yourusername/meeting-note-generator.git

cd meeting-note-generator
2.	**Set Up Python Environment**

Install the required Python packages:

pip install streamlit openai pydub python-docx

   3.	**Install BlackHole**
Follow the steps below to install and configure BlackHole for capturing audio.

## BlackHole Installation and Configuration

   1.	**Download and Install BlackHole**
   •	Download the BlackHole-2ch.pkg file from the project directory on GitHub.
   •	Open the downloaded .pkg file and follow the installation instructions.
   2.	**Verify Installation**
   •	Open the Audio MIDI Setup application on your Mac (found in Applications > Utilities).
   •	Click the + button at the bottom left corner and select Create Multi-Output Device.
   •	In the new Multi-Output Device, check the boxes next to BlackHole 16ch and your MacBook Air Speakers.
   3.	**Create Aggregate Device**
   •	In the Audio MIDI Setup, click the + button again and select Create Aggregate Device.
   •	Check the boxes next to MacBook Air Microphone and BlackHole 16ch.
   4.	**Set Aggregate Device as Input Source**
   •	Go to System Settings > Sound > Input tab and select Aggregate Device.
   5.	**Set Multi-Output Device as System Output**
   •	Go to System Settings > Sound > Output tab and select Multi-Output Device.

## Recording the Audio

   1.	**Open QuickTime Player**
   •	Open QuickTime Player and select File > New Audio Recording.
   2.	**Select Aggregate Device as Input Source in QuickTime**
   •	Next to the record button, click the small arrow and select Aggregate Device as the input source.
   3.	**Start Your Meeting**
   •	Join your Google Meet or Zoom meeting. Ensure that your system audio output is set to the Multi-Output Device.
   4.	**Record the Meeting**
   •	Start recording in QuickTime Player. This setup will capture both your microphone and the meeting audio.

## Running the Streamlit App

1.	**Set OpenAI API Key**
Set your OpenAI API key as an environment variable:

export OPENAI_API_KEY='your-openai-api-key'

2.	**Run the App**
Start the Streamlit app:

streamlit run app.py

**Usage**

   1.	**Upload Audio File**
   •	Upload your M4A recording through the Streamlit interface.
   2.	**Transcribe Audio**
   •	The app will convert the uploaded audio to MP3, transcribe it using OpenAI’s Whisper model, and display the transcribed text.
   3.	**Download Transcription**
   •	You can download the transcribed text as a plain text file.
   4.	**Summarize Transcription**
   •	Click the “Summarize” button to generate a summary of the transcription using GPT-4.
   5.	**Download Meeting Notes**
   •	Download the transcription and summary as a DOCX file.

## Troubleshooting

   •	Check System Preferences
Ensure QuickTime Player has permission to access your microphone in System Settings > Privacy & Security > Microphone.
   •	Restart Your Mac
After installing BlackHole and setting up devices, a restart can sometimes help in recognizing new audio devices.
   •	Recheck Connections
Make sure all checkboxes in the Audio MIDI Setup are correctly selected.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgements

   •	BlackHole by ExistentialAudio
   •	OpenAI for providing the Whisper and GPT-4 models
