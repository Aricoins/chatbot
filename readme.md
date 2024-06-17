Chatbot Program
Welcome to the Chatbot Program! This application allows you to have interactive conversations with a chatbot powered by OpenAI's GPT-4 model. Below, you will find instructions on how to set up, run, and use the program.

Features
Interactive chat with the GPT-4 model.
Keeps a history of the conversation within the session.
Colorful and user-friendly console interface.
Graceful handling of API errors.
Prerequisites
Before you can run the Chatbot Program, ensure you have the following installed:

Node.js (v14 or later)
npm (Node Package Manager)
Setup
Clone the repository:

bash
Copiar código
git clone <repository-url>
cd <repository-directory>
Install the dependencies:

bash
Copiar código
npm install
Configure OpenAI API:

Create a configuration file config/open-ai.js and add your OpenAI API key:

javascript
Copiar código
const { Configuration, OpenAIApi } = require('openai');

const configuration = new Configuration({
  apiKey: 'your-api-key-here',
});

const openai = new OpenAIApi(configuration);

module.exports = openai;
Running the Program
To start the Chatbot Program, run the following command in your terminal:

bash
Copiar código
node <script-name>.js
Replace <script-name> with the name of the file containing the chatbot code, for example, chatbot.js.

Usage
Once the program starts, you will be greeted with a welcome message.
You can start typing your messages after the prompt You: and press Enter.
The bot will respond with its message prefixed by Bot:.
To end the conversation, type exit.
Example Session
vbnet
Copiar código
Welcome to the Chatbot Program!
You can start chatting with the bot.

You: Hello, bot!
Bot: Hello! How can I assist you today?

You: Tell me a joke.
Bot: Why don't scientists trust atoms? Because they make up everything!

You: exit
Bot: Goodbye! Have a great day!
Error Handling
If the program encounters an error while communicating with the OpenAI API, it will display an appropriate error message in red text and terminate the session.

Customization
Chat History: The conversation history is stored in the chatHistory array. You can modify how the history is stored or displayed by editing the chatHistory logic.
Styling: The program uses the colors library to style the console output. You can customize the colors by referring to the colors.js documentation.
Dependencies
openai - For interacting with the OpenAI API.
readline-sync - For synchronous console input.
colors - For colorful console output.
License
This project is licensed under the MIT License. See the LICENSE file for details.