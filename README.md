============================================================
🎙️ Voice-Based Speaker Recognition Using MFCC and LSTM
============================================================

Project: Speaker Identification System
Course: ECE 5831 – Pattern Recognition and Neural Networks
University: University of Michigan – Dearborn
Team: Abbas Ali | Shravya Kumbham | Hesham Aldahbali
Date: December 2025

------------------------------------------------------------
📌 PROJECT OVERVIEW
------------------------------------------------------------
This project implements a voice-based speaker recognition system
that identifies who is speaking from short speech recordings.
The system uses Mel-Frequency Cepstral Coefficients (MFCCs) for
feature extraction and a Long Short-Term Memory (LSTM) neural
network to model temporal speech patterns.

Although the model achieved very high validation accuracy,
real-world testing revealed a critical issue: the model was
learning recording device characteristics instead of speaker
voice features. This project evolved into a controlled
experimental study that identified, proved, and fixed this issue.

------------------------------------------------------------
🎯 PROJECT GOALS
------------------------------------------------------------
- Build a robust speaker identification system from raw audio
- Validate MFCC + LSTM performance on public datasets
- Investigate real-world failure despite high validation accuracy
- Identify and eliminate confounding variables in data collection
- Achieve reliable cross-device speaker recognition

------------------------------------------------------------
📂 DATASETS USED
------------------------------------------------------------
1) Kaggle Dataset
   - Public speaker audio clips

2) YouTube Dataset
   - Speech extracted from public interviews

3) Custom Dataset
   - Speech recorded by team members

Dataset Split:
- Training:   70%
- Validation: 15%
- Testing:    15%

All audio was segmented into 1-second clips.

------------------------------------------------------------
🔧 PREPROCESSING PIPELINE
------------------------------------------------------------
- Download datasets from Kaggle and YouTube
- Record custom audio samples
- Convert all audio to WAV (uncompressed) format
- Segment audio into 1-second chunks using PyDub
- Remove silence, applause, music, and overlapping speech
- Extract MFCC features (32 x 13)
- Normalize and label data by speaker identity

------------------------------------------------------------
🧠 MODEL ARCHITECTURE
------------------------------------------------------------
Input:
- 32 x 13 MFCC feature matrices

Network:
- LSTM layer (128 units)
- Dense layer (64 units, ReLU)
- Output layer (Softmax)

Purpose:
- Learn temporal speaker-specific speech patterns
- Output probability distribution over speaker classes

------------------------------------------------------------
📊 EXPERIMENTAL PHASES
------------------------------------------------------------

Phase 1 & 2: Public Datasets (Kaggle + YouTube)
- High validation accuracy
- Confirmed correctness of MFCC + LSTM pipeline

Phase 3: Custom Dataset (Failure Case)
- Validation accuracy > 95%
- Real-world testing failed completely
- Model misclassified speakers with high confidence

Discovery:
- Model was learning microphone/device signatures
- Device type was perfectly correlated with speaker label

Phase 4: Controlled Data Collection (Solution)
- All speakers recorded using the SAME device
- Device signature became constant across classes
- Model forced to learn voice characteristics

------------------------------------------------------------
✅ FINAL RESULTS
------------------------------------------------------------
- Validation Accuracy: 95–98%
- Cross-Device Test Accuracy: ~96%
- Reliable speaker recognition on unseen recordings
- Demonstrated elimination of device bias

------------------------------------------------------------
🔑 KEY FINDINGS
------------------------------------------------------------
- Data collection is as important as model architecture
- High validation accuracy can be misleading
- Neural networks learn the easiest discriminative features
- Deployment-style testing is essential
- Controlled experiments reveal hidden biases

------------------------------------------------------------
⚠️ LIMITATIONS & FUTURE WORK
------------------------------------------------------------
- Increase number of speakers (10+)
- Apply data augmentation (noise, pitch shift, time stretch)
- Add attention mechanisms
- Speaker diarization (who spoke when)
- Anti-spoofing and replay attack detection
- Mobile authentication deployment
- Multimodal biometrics (voice + face)

------------------------------------------------------------
📚 REFERENCES
------------------------------------------------------------
[1] Davis & Mermelstein, IEEE TASSP, 1980
[2] Hochreiter & Schmidhuber, Neural Computation, 1997
[3] Reynolds & Rose, IEEE SAP, 1995
[4] Rabiner & Juang, Fundamentals of Speech Recognition
[5] Campbell, Proceedings of the IEEE, 1997

------------------------------------------------------------
✔ PROJECT HIGHLIGHT
------------------------------------------------------------
This project demonstrates that in machine learning systems,
data methodology can be just as important as algorithm design.



## Google drive Files Links

  - *Presentation Video:* 
  - *Presentation Slides:* https://drive.google.com/drive/folders/1QwCB7mRphUGjpWbzxYZqEJBjjyBBph5V?usp=sharing
  - *Project Report:* https://drive.google.com/drive/folders/1QwCB7mRphUGjpWbzxYZqEJBjjyBBph5V?usp=sharing
  - *Dataset:*
  - *Demo Video:* https://youtu.be/TUQWQDLSwyY