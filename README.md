# AI-Based Speech-Enabled Chatbot

This Python code implements a speech-enabled chatbot using various libraries for speech-to-text, text-to-speech, and language models. The chatbot is capable of understanding voice commands, responding in text, and converting the responses to speech.

## Requirements

Make sure you have the following Python libraries installed:

- [speech_recognition](https://pypi.org/project/SpeechRecognition/) for speech-to-text
- [gtts](https://pypi.org/project/gTTS/) for text-to-speech
- [transformers](https://huggingface.co/transformers/) for the language model

Install the required libraries using:

```bash
pip install SpeechRecognition
pip install gtts
pip install transformers
```

## Usage
1. Clone the repository:
```bash
git clone <repository_url>
cd <repository_directory>
```
2. Run the code:
```bash
python main.py
```
Speak to the chatbot and interact with it.

## Code Overview
### Libraries Used:
- `speech_recognition`: Used for converting speech to text.
- `gtts`: Used for converting text to speech.
- `transformers`: Used for the language model.

### ChatBot Class:
`__init__(self, name)`: Initializes the chatbot with a given name.
`speech_to_text(self)`: Captures speech input and converts it to text.
`text_to_speech(text)`: Converts the given text to speech.
`wake_up(self, text)`: Checks if the chatbot's name is mentioned in the input text.
`action_time()`: Returns the current time.

### Main Execution:
1. Initializes the chatbot and loads a conversational language model.
2. Enters a loop to continuously listen to user input.
3. Processes user input based on predefined conditions:
    - Wake Up: Responds with a greeting if the chatbot's name is mentioned.
    - Action Time: Responds with the current time if the word "time" is in the input.
    - Polite Responses: Responds politely to expressions of gratitude.
    - Exit: Responds with a farewell message and exits the loop.
    - Conversation: Uses a conversational language model to respond to general queries.
4. Converts the response to speech using `text_to_speech()`.
5. Continues the loop until the user decides to exit.

## Acknowledgments
The code utilizes the [microsoft/DialoGPT-medium](https://huggingface.co/microsoft/DialoGPT-medium?text=Hey+my+name+is+Clara%21+How+are+you%3F) language model from Hugging Face.


