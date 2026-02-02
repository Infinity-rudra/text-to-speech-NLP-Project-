Text-to-Speech Converter with gTTS
This Google Colab notebook provides a simple Python application to convert text into speech using the gTTS (Google Text-to-Speech) library. The generated audio is saved as an MP3 file and played directly within the Colab environment.

Features
Converts user-inputted text to spoken audio.
Uses gTTS for high-quality, natural-sounding speech.
Saves the audio as an MP3 file.
Plays the audio directly in Google Colab.
Getting Started
Prerequisites
To run this notebook, you only need a Google account and access to Google Colab.

Installation
Open the Notebook in Google Colab:

Go to Google Colab.
Upload this .ipynb file or open it from your Google Drive/GitHub if it's hosted there.
Install Required Libraries: The notebook automatically installs gtts as the first step.

!pip install gtts
Usage
Run all cells: Execute each code cell in sequence.

Enter Text: When prompted, enter the text you wish to convert to speech.

# The text that you want to convert to audio
mytext = input("Enter the text you want to convert to speech: ")

# Language in which you want to convert
language = 'en'

# Passing the text and language to the engine,
# here we have marked slow=False. Which tells
# the module that the converted audio should
# have a high speed
myobj = gTTS(text=mytext, lang=language, slow=False)

# Saving the converted audio in a mp3 file named
# welcome
myobj.save("welcome.mp3")

# Playing the converted file in Colab
Audio("welcome.mp3")
Listen to the Audio: An audio player will appear in the output of the last cell, allowing you to play the generated speech.

Project Structure
text_to_speech_colab.ipynb: The main Google Colab notebook containing all the code.
welcome.mp3: (Generated at runtime) The MP3 file containing the converted speech.
Contributing
Feel free to fork this repository, make improvements, and submit pull requests.

License
This project is open source and available under the MIT License.
