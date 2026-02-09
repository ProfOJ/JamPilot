# 🎸 JamPilot — Your AI Play-Along Band

> **Gemini 3 Global Hackathon 2025**

JamPilot is a real-time AI accompanist that **listens** to you sing or play, **detects** your musical key and tempo using Gemini 3, and **plays along** with genre-authentic chord progressions using Tone.js — all in your browser.

## 🎬 Demo

[Watch the 3-minute demo →](#) *(link to video)*

[Try it live →](#) *(link to deployed app or AI Studio)*

## How It Works

```
🎤 You sing/play  →  🧠 Gemini 3 analyzes  →  🎵 AI band plays along
        ↑                    ↓                         ↓
    Microphone         Key detection          Tone.js synthesizer
    (Web Audio)       Tempo analysis          Genre-specific patterns
                      Mood inference          Real-time chord progression
```

1. **Select your vibe** — Genre (Highlife, Afrobeats, Jazz, Reggae, Blues, etc.), locality (Ghana, Nigeria, Jamaica...), and accompaniment instrument
2. **Start singing or playing** — JamPilot captures your audio via the Web Audio API
3. **Gemini 3 listens & reasons** — Spectral analysis features are sent to Gemini, which uses music theory knowledge to detect your key, suggest tempo adjustments, and infer mood
4. **AI band kicks in** — Tone.js generates genre-authentic accompaniment with proper chord voicings, rhythm patterns, swing, and instrument layering

## 🧠 Gemini 3 Integration

JamPilot uses the **Gemini 3 API** (`gemini-2.5-flash`) as its musical brain:

- **Real-time audio reasoning**: Gemini receives spectral audio features (frequency distribution, amplitude, spectral centroid, zero-crossing rate) and applies music theory reasoning to determine the key being performed
- **Genre-aware intelligence**: The model is prompted with genre and locality context, enabling culturally-informed key detection (e.g., knowing Highlife favors certain keys and progressions)
- **Adaptive feedback loop**: Every 4 seconds, Gemini re-analyzes the audio and can trigger key changes, tempo adjustments, and mood shifts — the accompaniment reacts dynamically
- **Structured JSON output**: Uses `responseMimeType: 'application/json'` for reliable structured responses that drive the synth engine

This is **not** a prompt wrapper — Gemini is embedded in a continuous sense→reason→act loop that drives the entire musical experience.

## 🎵 Supported Genres & Localities

| Genre | Locality | Feel |
|-------|----------|------|
| 🇬🇭 Highlife | Ghana | Relaxed & Groovy |
| 🥁 Afrobeats | Nigeria | Driving & Percussive |
| 🎷 Jazz | USA | Smooth & Chromatic |
| 🇯🇲 Reggae | Jamaica | Off-beat & Laid-back |
| 🎸 Blues | USA | Soulful & Swinging |
| 🎤 Hip-Hop | USA/UK | Hard & Rhythmic |
| 🇿🇦 Amapiano | South Africa | Bouncy & Deep |
| ⛪ Gospel | Global | Uplifting & Rich |

## 🛠 Tech Stack

- **Gemini 3 API** — Musical key detection, tempo analysis, mood inference
- **Tone.js** — Web-based audio synthesis (guitar, bass, piano, drums, full band)
- **Web Audio API** — Real-time microphone capture and spectral analysis
- **Vanilla HTML/CSS/JS** — Zero-dependency frontend, runs in any browser

## 🚀 Quick Start

1. Get a free Gemini API key at [Google AI Studio](https://aistudio.google.com/apikey)
2. Open `index.html` in your browser (or visit the live demo)
3. Enter your API key
4. Select genre, locality, and instrument
5. Hit **Start Jamming** and start singing or playing!

## 📁 Project Structure

```
jampilot/
├── index.html      # Complete single-file app (UI + synth engine + Gemini integration)
└── README.md       # This file
```

## 🏆 Built For

[Gemini 3 Global Hackathon](https://devpost.com/) by Google DeepMind

**Track**: The Real-Time Teacher / Creative Autopilot

## 👤 Author

**Joshua Odoi** — Fullstack Developer & Tech Innovation Lead
- GitHub: [@profoj](https://github.com/profoj)
- LinkedIn: [profoj](https://linkedin.com/in/profoj)
- Email: odoijoshua55@gmail.com

---

*JamPilot: Because every musician deserves a band that never misses rehearsal.* 🎸
