# Shell Command Plugin - CommandGPT

<img src="https://github.com/S-Vismaya/CommandGPT/blob/main/.well-known/logo.png" alt="Command GPT" title="Command GPT Logo" width="200" height="200">

The CommandGPT Plugin is a simple Flask-based API that allows users to execute shell commands and receive the results in JSON format. The plugin listens on `localhost:3333` and provides an endpoint `/run` that accepts a shell command as a query parameter and returns the output of the command as a JSON response. This is meant to be used with the OpenAI ChatGPT plug-in system.

The software is currently ALPHA so use it at your own risk.


## Getting Started

### Prerequisites

- Python 3
- Flask
- Flask-CORS

### Installation

1. Clone the repository:  
   `git clone https://github.com/S-Vismaya/CommandGPT.git`
   
2. Change to the project directory:  
   `cd CommandGPT`
   
3. Install the requirements:  
   `pip install -r requirements.txt`
   
### Running the Plugin

1. Start the Flask server:  
   `python main.py`
   
2. Test the API using `curl` or a similar tool:  
   `curl "http://localhost:3333/run?command=ls"`

### Setup in ChatGPT

From ChatGPT, select to add a plug-in via the PlugIn Store. You will need to select that you want to develop your own plug-in. It will now allow you to enter the URL of your local plugin script. If the above test worked, then you should be able to enter `http://localhost:3333` into the custom prompt to let it add your plugin.

