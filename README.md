# Academic Voice Research Assistant

A local voice assistant designed for students and researchers in AI and machine learning.

**Pipeline:** Microphone → Faster-Whisper → Ollama (Llama 3.2) → Piper TTS → Speaker

Fully runnable from Google Colab on the free tier.

## Features

- Speech-to-text using Faster-Whisper
- Local language model via Ollama (Llama 3.2 3B)
- Natural text-to-speech with Piper
- Browser-based microphone input through Gradio
- Conversation history with context
- Optimized for short, spoken academic explanations

## Intended Use Cases

- Explaining research concepts in plain language
- Clarifying methods, architectures, or papers
- Refining paper ideas or abstracts verbally
- Practicing research presentations
- Quick technical discussions without typing

## Quick Start with Google Colab

1. Open the notebook directly in Colab:

   [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RamGhadiyaram/academic-voice-research-assistant/blob/main/Voice_Research_Assistant.ipynb)

2. Runtime → Change runtime type → **T4 GPU** (recommended)

3. Run all cells in order

4. Allow microphone access when the browser requests it

5. Speak and the assistant will reply with voice

## Requirements

- Google Colab (free tier is sufficient)
- Microphone access in the browser
- Approximately 5–8 GB of free disk space for models (downloaded automatically)

## Model Choices

| Component       | Default              | Notes                          |
|-----------------|----------------------|--------------------------------|
| Speech-to-Text  | Whisper `base`       | Fast and accurate enough      |
| Language Model  | `llama3.2:3b`        | Good balance for Colab        |
| Text-to-Speech  | `en_US-lessac-medium`| Clear and natural             |

You can change the Ollama model or Piper voice by editing the corresponding cells.

## Local Installation (Optional)

If you prefer to run outside Colab:

```bash
pip install faster-whisper piper-tts gradio ollama soundfile numpy
# Install Ollama from https://ollama.com
ollama pull llama3.2:3b
python -m piper.download_voices en_US-lessac-medium
```

Then open and run the notebook locally or convert the core logic into a pure Python script.

## License

This project is provided as-is for educational and research purposes.
