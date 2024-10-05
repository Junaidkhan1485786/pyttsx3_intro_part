pyttsx3 is a Python library that allows you to convert text to speech (TTS). It works offline and is compatible with both Python 2 and 3. Here's a brief introduction to getting started with pyttsx3.

Installation
You can install pyttsx3 using pip:
pip install pyttsx3


Basic Usage
Here’s a simple example of how to use pyttsx3 to convert text to speech:
import pyttsx3

# Initialize the TTS engine
engine = pyttsx3.init()

# Set properties (optional)
engine.setProperty('rate', 150)    # Speed of speech
engine.setProperty('volume', 0.9)  # Volume level (0.0 to 1.0)

# Text to be spoken
text = "Hello, welcome to pyttsx3 tutorial!"

# Speak the text
engine.say(text)

# Wait until the speech is finished
engine.runAndWait()

Key Features
Voice Control: You can change the voice to male or female, depending on the voices installed on your system.
