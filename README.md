# ESP32-S3 Voice Assistant Using ChatGPT

This repository hosts the source code for a voice assistant designed for the ESP32-S3 chip using the Arduino Framework. It incorporates a wake word detection feature using a neural network that responds to the word "komputer". The assistant leverages the Google STT API for speech-to-text, ChatGPT API for natural language understanding, and a Speech Synthesizer module based on Microlena for text-to-speech capabilities.

## Table of Contents
- [System Overview](#system-overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)

## System Overview

The project is divided into several modules that together form the entire voice assistant system.

1. **I2S Sampler**: This module is responsible for handling the audio input.
2. **Command Detector**: Processes the input to identify possible command triggers.
3. **Neural Network**: Trained to recognize the wake word "komputer", triggering the voice assistant.
4. **Google STT API**: Converts spoken language into written text that can be processed.
5. **ChatGPT API**: Processes the converted text to understand the request.
6. **Speech Synthesizer (Microlena)**: Converts processed response text back into spoken language.

## Prerequisites

- An ESP32-S3 chip.
- [Espressif toolset](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html) for building and uploading the code to ESP32-S3.
- A service account on [Google Cloud](https://cloud.google.com/docs/authentication/getting-started).
- An account on [OpenAI](https://beta.openai.com/docs/developer-quickstart/) with a valid API token.

## Installation

Follow these steps to get the voice assistant running:

1. **Clone the Repository**

   ```
   git clone https://github.com/chwalap/wake-word-komputer-firmware.git
   ```

2. **Build the Project**

   Use PlatformIO to build the project.

3. **Upload the Project**

   Upload the built project to your ESP32-S3 chip using the esptool.

4. **Google Cloud Service Account**

   Set up your service account on Google Cloud and download your credentials. Update the relevant sections of the code with these credentials.

5. **OpenAI API Token**

   Register on OpenAI and get your API token. Update the respective section in the code with this token.

## Usage

After setting up the device and credentials, the voice assistant is ready for use. Activate it by saying the wake word "komputer", followed by your command. For example:

```
"komputer, what is the weather today?"
```
