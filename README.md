
# Groq API Integration Project

## Table of Contents
- [Overview](#overview)
- [Setup Instructions](#setup-instructions)
  - [Step 1: Create an Anaconda Environment](#step-1-create-an-anaconda-environment)
  - [Step 2: Install Required Packages](#step-2-install-required-packages)
  - [Step 3: Obtain a Groq API Key](#step-3-obtain-a-groq-api-key)
  - [Step 4: Configure the .env File](#step-4-configure-the-env-file)
- [Description of Provided Notebooks](#Description-of-Provided-Notebooks)
- [Running the Application](#Running-the-Application)  
- [Using Jupyter Notebooks in VS Code](#using-jupyter-notebooks-in-vs-code)
- [Description of Provided Notebooks](#description-of-provided-notebooks)
- [Task Details](#task-details)
- [Reflection on the Experience](#reflection-on-the-experience)
- [Submission Checklist](#submission-checklist)



## Overview
This project demonstrates how to integrate with the Groq API to generate a creative "Hello World" message. It uses Python and leverages Anaconda for environment management. The project also includes text-to-speech functionality, allowing the response to be read aloud.

### Project Structure
- **Code Files**: Contains the Jupyter Notebook (`GroqAPI.ipynb` and `GroqAPInteractive.ipynb`) which details code and steps to integrate the Groq API and generate text output.
- **Documentation**: The README file explains installation, API setup, and application usage.
- **Reflection**: Included in the README under “Reflection on the Experience.”

---

## Setup Instructions

### Step 1: Create an Anaconda Environment

1. Open your terminal or Anaconda Prompt install [Anaconda](https://docs.anaconda.com/anaconda/install/) for your system .
2. Run the following command to create a new environment:

    ```bash
    conda create -n groq_api_env python=3.10
    ```

3. Activate the environment:

    ```bash
    conda activate groq_api_env
    ```

### Step 2: Install Required Packages

Install the necessary packages, including `pyttsx3` for text-to-speech and `pyaudio` (often a dependency for TTS systems), as well as other required libraries:

```bash
pip install groq dotenv pyttsx3 pyaudio SpeechRecognition
```

**Packages Overview**:
- `groq`: Library to interact with the Groq API.
- `dotenv`: Manages environment variables securely.
- `pyttsx3`: Handles offline text-to-speech.
- `pyaudio`: Enables audio output for `pyttsx3`.
- `SpeechRecognition` : Enables to convert speech to text

### Step 3: Obtain a Groq API Key

1. Visit the [Groq API website](https://www.groq.com) and sign up for a developer account.
2. Generate a free API key from your dashboard under **API Keys**.
3. Copy this key for use in the next step.
4. I have also provided a key for ease of useage in the APIKEY.txt

### Step 4: Configure the `.env` File

1. In the root directory of your project, create a `.env` file (if it doesn’t already exist).
2. Add your Groq API key in the following format:

    ```plaintext
    GROQ_API_KEY=your_api_key_here
    ```

3. For security, ensure `.env` is listed in `.gitignore` (included in this project) to avoid accidentally committing sensitive information.

---
## Description of Provided Notebooks

This repository includes the following `.ipynb` files:

- **GroqAPI.ipynb**: This notebook demonstrates the core integration with the Groq API, including setting up the API key, making a request to the API, and converting the response to speech output. It serves as the main example of how to interact with Groq and generate conversational responses.

- **GroqAPInteractive.ipynb**: An interactive notebook that expands on the initial setup by including examples for handling user prompts in real time. It provides an interactive way to input text and see Groq API responses, showcasing practical usage scenarios of conversational AI.

These descriptions should help you understand the purpose and usage of each notebook included in the project.

---
## Running the Application

1. **Load Environment Variables**: The application uses `dotenv` to load environment variables from `.env`.
2. **Make an API Request**:
    - This project sends a message to the Groq API and retrieves a response.
    - The text response is processed and outputted as both text and audio.

### Instructions

- Open and run the `GroqAPI.ipynb` notebook in Jupyter to execute each cell step-by-step. This is the basic implementation of plugging in the API with a few options for proppts you can select from.
- When you reach the final cell, the API will generate a response to your input prompt.
- The response will display in the console and be read aloud by the TTS system.

- Following this run `GroqAPInteractive.ipynb` this is an interactive voice based code. 
- On running all the cells it will give you a set of options of microphones from your local system. Choose any known microphone (incase 1st choice doest work try a few other options).
- Speak to the system and it will answer your questions. 

---

## Task Details

### API Selection

We selected the **Groq API**, a generative AI API that supports multiple model integrations, including LLaMA for large language models.

### Application Development

The notebook script connects to the Groq API and uses the API to generate responses based on user prompts, providing a conversational response from the LLaMA model.

### "Hello World" Generative Task

The application is pre-configured to output a "Hello World" conversation prompt, introducing the Groq API in a conversational style.

### Documentation

The code in the notebook is documented, and instructions for setup and usage are in this README.

---

## Reflection on the Experience

### Challenges
Integrating the Groq API was smooth, by using the API i did not face any challenges.

### Key Learnings
This project highlighted the flexibility of generative AI APIs in creating dynamic, conversational outputs. It reinforced the importance of secure environment variable handling and API key management for application security.By using the API I did not have to worry about compute power of my laptop and setup of different package to ensure the LLM runs on gpu for fast responses as the API takes care of this in the backend at the server it is acessing.

### Future Applications
This experience opens opportunities to leverage generative AI APIs for applications , real-time language translation, help blind people interact with something like `GroqAPInteractive.ipynb` . My final project for AI-HCI class is built on the same idea.

---

## Submission Checklist

- **Code Files**: Ensure `GroqAPI.ipynb`, `GroqAPInteractive.ipynb`,`.env`, and `.gitignore` files are included.
- **Documentation**: This README file serves as both documentation and reflection.
- **Submission**: Zip all files or push them to a GitHub repository and share the link.


## Using Jupyter Notebooks in VS Code

### Adding the Jupyter Notebook Extension
To work with Jupyter Notebooks in Visual Studio Code (VS Code), you need to install the Jupyter extension:
1. Open VS Code.
2. Go to the Extensions view by clicking on the square icon in the sidebar or by pressing `Ctrl+Shift+X` (Windows/Linux) or `Cmd+Shift+X` (Mac).
3. Search for "Jupyter" and install the extension provided by Microsoft.

This extension allows you to open, view, and run `.ipynb` notebook files directly in VS Code.

### Selecting the Environment for the Jupyter Kernel
After creating your new environment (`groq_api_env`), you can select it as the kernel in VS Code to ensure the notebook uses the correct environment and packages:
1. Open a Jupyter Notebook file (`.ipynb`) in VS Code.
2. Click on the kernel name at the top right of the notebook interface.
3. In the dropdown, select your environment (`groq_api_env`). If you don’t see it, you may need to restart VS Code or check that the environment is properly activated.

This setup ensures that your notebook will use all packages installed in the `groq_api_env` environment.

---

