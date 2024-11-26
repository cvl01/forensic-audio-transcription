# Forensic Audio Transcription

This repository bundles the code supporting my research on forensic audio transcription. 

This research was conducted from April - November 2024, at the Dutch Safety Board, as research project for my Master Forensic Science at the University of Amsterdam  
📄 View paper: [Master Thesis](thesis.pdf)

## Repositories

### WhisperX
My WhisperX implementation adds additional options for detection of language every 30 seconds, for improved multi-language audio handling, as described in my paper. Also includes some other nice improvements. Pull request is pending, but as of now the [original](https://github.com/m-bain/whisperX) WhisperX repository seems unmaintained. 

🔗 https://github.com/cvl01/whisperX

### Transcript server
I created a FastAPI transcript server to process requests for audio transcription, and summarization, correction and analysis using local LLM's. It also contains an optional Vocal Separation preprocessing step. For details, I refer to my paper.

Next to the FastAPI server, I created a Web UI using Vue. 

🔗 https://github.com/cvl01/ovv-transcript-server (FastAPI server)  
🔗 https://github.com/cvl01/ovv-transcript-server-ui (Vue UI)

### Whisper tuning scripts
The scripts I used for finetuning Whisper and creating a better-performing Whisper model for the OVV have also been bundled in a repository. PEFT methods were used, both AdaLoRa and LoRa. Evaluation code is also included. 

🔗 https://github.com/cvl01/whisper-peft-training-scripts

## Dataset creation using alignment of interview audio
To generate a dataset based on long audio (1+ h) I created alignment and splitting code using methods implemented in [echogarden](https://github.com/echogarden-project/echogarden). This set of scripts to replicate creating a dataset from this type of material can be found here.

🔗 https://github.com/cvl01/align-segments-using-echogarden-for-whisper
