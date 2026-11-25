# Cali — Voice-Enabled Virtual Assistant

A desktop voice assistant built in Python using `SpeechRecognition` for speech-to-text, `pyttsx3` (Windows SAPI5) for speech synthesis, and third-party APIs for weather, Wikipedia summaries, and computational queries.

---

## Demo

<p align="center">
  <img src="Cali-demo.gif" width="760" alt="Cali Voice Assistant Demo" />
</p>

<p align="center">
  <img src="Cali1.png" width="380" alt="Cali console session 1" />
  <img src="Cali2.png" width="380" alt="Cali console session 2" />
</p>

---

## Features

| Voice Command | Action |
| :--- | :--- |
| `"open youtube"` / `"open google"` / `"open gmail"` / `"open stackoverflow"` | Opens the requested site in your browser |
| `"what is the time"` | Reads the current local time |
| `"weather"` | Prompts for a city and reads temperature, humidity, and forecast via OpenWeatherMap |
| `"wikipedia <topic>"` | Fetches and reads a 3-sentence summary from Wikipedia |
| `"ask"` | Prompts for a computational or geographical question via WolframAlpha |
| `"news"` | Opens LA Times top headlines in the browser |
| `"camera"` / `"take a photo"` | Captures a photo from the webcam (`img.jpg`) |
| `"search <query>"` | Searches the query in the browser |
| `"good bye"` / `"ok bye"` / `"stop"` | Shuts down the assistant |
| `"log off"` / `"sign out"` | Signs out of the Windows session |

---

## Setup & Usage (Windows)

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

> **Note:** On Windows, `pyaudio` may require `pipwin install pyaudio` if a prebuilt wheel is unavailable for your Python version. The assistant uses Windows `sapi5` via `pyttsx3`.

### 2. Configure API Keys

Copy `.env.example` and export your keys before running:

```bash
# PowerShell
$env:OPENWEATHER_API_KEY="your_openweathermap_key"
$env:WOLFRAMALPHA_APP_ID="your_wolframalpha_app_id"
```

### 3. Run

```bash
python Cali.py
```

---

## Repository Contents

- `Cali.py` — Main voice recognition loop and command handlers
- `requirements.txt` — Third-party pip dependencies (`SpeechRecognition`, `pyttsx3`, `wikipedia`, `wolframalpha`, `ecapture`, `requests`, `pyaudio`)
- `.env.example` — Environment variable template for OpenWeatherMap and WolframAlpha
