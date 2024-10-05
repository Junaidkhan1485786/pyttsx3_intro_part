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
voices = engine.getProperty('voices')
engine.setProperty('voice', voices[1].id)  # Set to female voice (usually index 1)
Adjustable Speech Rate: The speed of the speech can be modified using the setProperty method.

Volume Control: The volume of the speech can also be adjusted.

Events: You can attach event listeners to get callbacks when the speech starts, ends, or encounters an error.
Example with Voice Selection
Here’s a more advanced example demonstrating voice selection and event handling:
 bash ```
 import pyttsx3

def onStart(name):
    print(f'Speech started for {name}')

def onEnd(name, completed):
    print(f'Speech ended for {name}. Completed: {completed}')

engine = pyttsx3.init()
engine.connect('started-utterance', onStart)
engine.connect('finished-utterance', onEnd)

# Choose a voice
voices = engine.getProperty('voices')
engine.setProperty('voice', voices[0].id)  # Change index for different voices

engine.say("This is an example of text to speech with pyttsx3.")
engine.runAndWait()
```

Conclusion
pyttsx3 is a straightforward and powerful library for text-to-speech conversion in Python. It's useful for creating applications that require audio output, such as accessibility tools, interactive applications, or educational software.

