# Lazarus AI
### What is this project?
`lazarus` is a hobby project with the ultimate goal of being able to accurate capture your "personality" through recorded conversations and emulate it using a language model in conjunction with a voice cloning model.
### How does it work?
There are several steps:
- Record numerous conversations you partake in with other people
- Post-process the audio files of the conversations to create conversation transcripts
	- Reduce background noise using `noisereduce`
	- Perform speaker diarization (who says what in the conversation) using `pyannote.audio`
	- Transcribe what each speaker says using `openai-whisper`
	- Create a transcript of the conversation
- Use the conversation transcripts to in conjunction with an LLM (either by prompt engineering or fine-tuning) to properly emulate your personality, including traits like common words used, temperament, and conversational style
- Layer in a voice cloning model that will emulate your voice style, including traits like intonation, cadence, and inflection
### How far along is the project?
Right now, the codebase is able to process individual raw audio files into full conversation transcripts with relatively high accuracy. Currently, there is no user interface and all processing must be done in a Jupyter notebook. I am in the process of recording enough conversations to proceed to the next step, which is using an LLM to emulate someone's personality. I will update this codebase as I make progress.