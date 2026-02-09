# Submission: Gemini Integration Description (~200 words)

## JamPilot — Your AI Play-Along Band

JamPilot transforms Gemini 3 into a real-time musical accompanist. Select a genre (Highlife, Afrobeats, Jazz, Reggae, Blues, Amapiano, Hip-Hop, Gospel), choose your locality and instrument, then start singing or playing. JamPilot listens through your microphone, and Gemini 3 becomes your bandmate.

**Gemini 3 Features Used:**

- **Real-Time Audio Reasoning**: The Web Audio API captures microphone input and extracts spectral features (peak frequency, amplitude, spectral centroid, zero-crossing rate). These features are sent to Gemini 3 every 4 seconds in a continuous sense→reason→act loop.

- **Music Theory Intelligence**: Gemini receives audio features with genre and cultural context, then applies music theory reasoning to determine the musical key, suggest tempo adjustments, and infer mood — outputting structured JSON that drives the Tone.js synthesizer.

- **Adaptive Feedback Loop**: This is not a one-shot analysis. Gemini continuously re-evaluates the performance, triggering key changes, tempo ramps, and mood shifts. The accompaniment evolves with the performer.

- **Genre-Aware Cultural Context**: Prompts include locality context (Ghana, Nigeria, Jamaica), enabling Gemini to make culturally-informed decisions about chord progressions and musical feel.

Gemini 3 is central — without it, there's no key detection, no adaptation, and no AI band. It's the brain that makes JamPilot listen and react.
