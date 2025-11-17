
<img width="800" alt="IMG_6610" src="https://github.com/user-attachments/assets/49a65ceb-85a6-4446-b333-78071e0c541c" />

# Bug

A portable audio capture device paired with an iOS app for hands-free recording and AI-powered study assistance.

## Overview

Bug is a full-stack real-time audio pipeline that captures spoken content, transcribes it, and transforms it into interactive study materials. The system combines custom embedded firmware, optimized mobile networking, and cloud transcription to deliver a seamless recording experience.

## Key Achievements

- **95% reduction in BLE packet loss** through optimized batching protocol
- **Real-time transcription pipeline** with sub-second latency
- **End-to-end audio streaming** from hardware to cloud with automatic reconnection
- **AI-generated flashcards** from recorded transcripts for active learning

## Architecture

**Hardware (ESP32-S3)**  
Custom firmware captures 16 kHz PCM audio via I2S microphone, buffers it in a ring buffer, and streams efficiently over Bluetooth Low Energy.

**Mobile (iOS)**  
Native Swift app manages BLE connection with the Bug device, handles real-time audio streaming, and provides an interactive UI, with gamified flashcard generation.

**Backend (Node.js + Fastify)**  
WebSocket server processes incoming PCM audio streams with lazy initialization, delivers real-time STT transcription, and manages session state with automatic reconnection.

## Repository Links

- **[Firmware](https://github.com/iancarscadden/bug_firmware)** – ESP32-S3 embedded code for audio capture and BLE streaming
- **[iOS App](https://github.com/iancarscadden/bug_ios)** – Swift mobile app for device pairing and study tools *(may be private)*
- **[Backend](https://github.com/iancarscadden/bug_backend)** – Node.js WebSocket server for real-time transcription

---

Built with ESP32-S3, Swift, Bluetooth Low Energy, WebSockets, and speech-to-text APIs.
