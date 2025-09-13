
# Call Quality Analyzer with Speaker Diarization

This project is a complete system to analyze sales or customer calls. It transcribes audio, identifies speakers, and provides insightful metrics about the call. It is built using Python, Whisper, and Pyannote (with fallback for diarization), and is fully runnable in Google Colab.

### Brief Explanation of Approach

This project performs automatic transcription and speaker diarization of audio files. The workflow first downloads audio, then uses Whisper to transcribe the speech into text segments. Next, a speaker diarization model identifies and labels speakers across the audio timeline. Finally, the transcription segments are merged with the diarization results to produce a final transcript with speaker labels and timestamps. This approach allows for clear identification of who said what and when, making it useful for meetings, interviews, and call analysis.




## Features

- Download audio from YouTube links.

- Automatic transcription using OpenAI Whisper.

- Speaker diarization with Pyannote (or fallback energy-based method).

- Merges transcription with speaker segments to generate a clear final transcript.

- Provides call analytics:

    - Talk-time ratio per speaker

    - Number of questions asked

    - Longest monologue

    - Call sentiment (positive/neutral/negative)

    - Actionable insights

- Bonus: Identifies the sales representative vs customer.

- Optimized to run in <30 seconds on free Colab tier.


## 🔗 Open and run the notebook in Google Colab
[![Google Colab](https://img.shields.io/badge/Google_Colab-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://colab.research.google.com/drive/1wyRTaJ6Hm5IMBngpHTmWsN5nftC8qmnc?usp=sharing/)


