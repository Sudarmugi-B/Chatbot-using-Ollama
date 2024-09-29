# Ollama-based Chatbot

This project implements a simple chatbot using Streamlit and Ollama, a local language model server. The chatbot uses the "guru" model from Ollama to generate responses.

## Features

- Web-based chat interface using Streamlit
- Integration with Ollama for local language model inference
- Conversation history maintained throughout the session

## Screenshots

Here are some screenshots of the chatbot in action:

### Initial Interaction
![Initial Chatbot Interaction](chatbot_screenshot_1.png)
*Screenshot showing the initial interaction with the chatbot*

### Generating Content
![Chatbot Generating Content](chatbot_screenshot_2.png)
*Screenshot displaying the chatbot generating a poem about generative AI*

These screenshots demonstrate the user interface and some capabilities of the chatbot, including basic conversation and content generation.

## Prerequisites

- Python 3.6+
- Streamlit
- OpenAI Python library
- Ollama

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/Sudarmugi-B/Chatbot-using-Ollama
   cd ollama-chatbot
   ```

2. Install the required Python packages:
   ```
   pip install streamlit openai
   ```

3. Install Ollama:
   - Visit [Ollama's official website](https://ollama.ai/) for installation instructions specific to your operating system.

4. Install the language model of your choice using Ollama. For example, to install the Llama 2 model:
   ```
   ollama pull llama2
   ```

## Usage

1. Start the Ollama server with your chosen model. For example, to run the Llama 2 model:
   ```
   ollama run llama2
   ```

2. In a new terminal window, run the Streamlit app:
   ```
   streamlit run chat.py
   ```

3. Open your web browser and navigate to the URL provided by Streamlit (usually `http://localhost:8501`).

4. Start chatting with the bot by typing your questions or messages in the input field.

## How it Works

- The application uses Streamlit to create a web-based chat interface.
- It initializes a conversation with a system message defining the assistant's role.
- User inputs are sent to the Ollama server using the OpenAI API format.
- Responses from the chosen model (currently set to "guru" in the code) are displayed in the chat interface.
- The conversation history is maintained throughout the session using Streamlit's session state.

## Customization

- To use a different Ollama model, change the `model` parameter in the `conversation.message()` method in `chat.py`. Make sure to install and run the corresponding model with Ollama.
- Adjust the system message in the `message_list` initialization to modify the assistant's behavior.

## Note

This project uses Ollama, which runs models locally on your machine. Make sure you have sufficient computational resources to run the chosen model. Different models may have different resource requirements.

