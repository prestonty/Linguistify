# Linguistify

**Linguistify** is a video dubbing software designed to automate the dubbing of YouTube videos into different languages. Inspired by creators like MrBeast who operate multiple channels in different countries and hire professional voice actors (which is very expensive), this tool offers a more affordable, AI-powered solution for multilingual dubbing.

---

## Table of Contents

1. [Features](#features)  
2. [Tech Stack](#tech-stack)  
3. [Workflow](#workflow)  
4. [Setup & Installation](#setup--installation)  
5. [Usage](#usage)  
6. [Configuration](#configuration)  
7. [Contributing](#contributing)  
8. [License](#license)  
9. [Authors & Acknowledgements](#authors--acknowledgements)

---

## Features

- Automatically dubs YouTube videos into different languages
- Timestamp-level utterance tracking for precise sync
- Translates and adapts spoken content to fit timing constraints
- Generates smooth, natural-sounding speech using AI voices
- Outputs a fully dubbed video or audio track

---

## Tech Stack

- **Backend**: Flask  
- **Frontend**: React with Chakra UI  
- **Speech-to-Text**: Deepgram  
- **Voice Generation**: ElevenLabs  
- **NLP & Processing**: Hugging Face, OpenAI GPT  
- **Translation**: DeepL  
- **AI Framework**: PyTorch

---

## Workflow

1. **Speech-to-Text**  
   - Deepgram transcribes video and identifies timestamped utterances.

2. **Translation**  
   - Transcribed text is translated into the target language using DeepL.

3. **Timing Alignment**  
   - OpenAI GPT rewords translated utterances to match original durations.

4. **Audio Generation**  
   - ElevenLabs generates speech for each utterance, including pauses.

5. **Stitching**  
   - Generated audio is stitched into the original video for final output.

---

## Setup & Installation

```bash
# Clone the repo
git clone https://github.com/prestonty/Linguistify.git
cd Linguistify

# Backend setup
cd flaskbackend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Frontend setup
cd ../reactfront
npm install
