
# WhisperClip: One-Click Audio Transcription

WhisperClip simplifies your life by automatically transcribing audio recordings and saving the text directly to your clipboard. With just a click of a button, you can effortlessly convert spoken words into written text, ready to be pasted wherever you need it. This application harnesses the power of OpenAI's Whisper for free, making transcription more accessible and convenient.

![Example using WhisperClip](./readme_assets/example-of-usage.gif)

## Features

- Record audio with a simple click.
- Automatically transcribe audio using Whisper (free).
- Option to save transcriptions directly to the clipboard.

## Installation

### Prerequisites

- Python 3.8 or higher
- [CUDA](https://developer.nvidia.com/cuda-downloads) compatible with PyTorch. Refer to [PyTorch's website](https://pytorch.org/get-started/locally/) for compatibility information.

### Setting Up the Environment

1. Clone the repository:
   ```
   git clone https://github.com/your-username/whisper-clip.git
   cd whisper-clip
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

### Choosing the Right Model

Based on your GPU's VRAM, choose the appropriate Whisper model for optimal performance. Below is a table of available models with their required VRAM and relative speed:

|  Size  | Required VRAM | Relative speed |
|:------:|:-------------:|:--------------:|
|  tiny  |     ~1 GB     |      ~32x      |
|  base  |     ~1 GB     |      ~16x      |
| small  |     ~2 GB     |      ~6x       |
| medium |     ~5 GB     |      ~2x       |
| large  |    ~10 GB     |       1x       |

For English-only applications, `.en` models (e.g., `tiny.en`, `base.en`) tend to perform better.

To change the model, modify the `model_name` variable in `whisper_client.py` to the desired model name.

## Usage

Run the application:

```
python main.py
```

- Click the microphone button to start and stop recording.
- If "Save to Clipboard" is checked, the transcription will be copied to your clipboard automatically.

## Acknowledgments

This project uses [OpenAI's Whisper](https://github.com/openai/whisper) for audio transcription.
