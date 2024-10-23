# Google Generative AI Chatbot

This Python script uses the Google Generative AI API to create an interactive chatbot. The bot responds to user input using the gemini-1.5-flash model. The script is fully configurable, allowing you to adjust temperature, token limits, and other generation settings. You can start a chat session, send messages, and receive responses in real-time.

## Features
Real-time chatbot interaction using Google Generative AI.
Customizable generation settings, including temperature, top_p, top_k, and token limits.
Simple and intuitive command-line interface.
Easy to configure API key for authentication.
Supports safety settings for content moderation.

## Prerequisites
Before running the script, you need the following:

Python 3.x installed on your machine.
A valid Google Generative AI API key.

### Install the required dependencies:
Make sure you have the google-generativeai package installed. If not, you can install it using: !pip install google-generativeai

### Set up your API key:
Obtain your API key from the Google Cloud Console.
Replace the placeholder API_KEY in the script with your actual API key: genai.configure(api_key="YOUR_API_KEY")

Start interacting with the chatbot by typing messages in the console. Type exit or quit to stop the chat session.
#### Example:
You: Hello
Bot: Hi! How can I assist you today?

### Configuration
You can modify the chatbot’s behavior by adjusting the generation settings in the generation_config:
temperature: Controls the randomness of the output. Higher values (closer to 1) will result in more creative responses, while lower values will make responses more focused and deterministic.
top_p: Determines the cumulative probability for token sampling. A value of 0.95 ensures that tokens are sampled from the top 95% of the probability mass.
top_k: Limits token selection to the top k tokens, ensuring more predictable outputs.
max_output_tokens: Sets the maximum number of tokens in the bot's response.

#### Example configuration:
generation_config = {
    "temperature": 0.7,
    "top_p": 0.9,
    "top_k": 50,
    "max_output_tokens": 500,
}

### Safety Settings
The script includes links for managing safety settings directly from the API. You can adjust content moderation by configuring safety filters:
Visit Google Generative AI Safety Settings for more information on how to enable or disable certain filters.

### License
This project is licensed under the MIT License.

