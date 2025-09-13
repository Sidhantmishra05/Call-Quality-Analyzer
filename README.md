# Call-Quality-Analyzer

### Approach Overview

Our Call Quality Analyzer processes sales call recordings to provide actionable insights efficiently. First, the audio is downloaded and converted to a clean .wav format. We use OpenAI’s Whisper model for transcription, splitting the call into time-stamped text segments. Simultaneously, speaker diarization is performed using a fallback energy-based method (or Pyannote if authenticated), identifying who spoke when.

Next, we combine the transcription with speaker segments, aligning text with each speaker. This enables calculation of metrics like talk-time ratio, longest monologue, and the number of questions asked per participant. Sentiment analysis is applied on each speaker’s utterances to classify them as positive, negative, or neutral. Finally, the system generates one actionable insight, such as balancing speaking time or improving engagement.

We designed the pipeline to handle poor audio quality, run under 30 seconds on the free Colab tier, and produce clear outputs for analysis. The notebook is modular, making it easy to extend features like automatically detecting the sales rep versus the customer, visualizing speech patterns, or integrating other AI models in the future.
