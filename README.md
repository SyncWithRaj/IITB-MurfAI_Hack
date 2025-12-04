# 🎭 Murf’s Got Latent  
### Voice-First 3D Improv Battle — Murf's Got Latent

## 🎥 Demo Video (Click on Thumbnail to Watch Demo)

[![Watch the video](https://img.youtube.com/vi/MqjIZV65QaA/maxresdefault.jpg)](https://youtu.be/MqjIZV65QaA)

**Murf’s Got Latent** is a fully immersive, voice-controlled 3D improv game show.  
Instead of a normal chatbot, you perform on a **real-time 3D stage**, where an AI Host (LLM + ultra-low latency TTS) interacts with you like a real Indian reality show judge.

The system listens to your performance, evaluates your creativity, and responds instantly with roasts, praise, applause, and dynamic stage lighting — all lip-synced and animated.

---

## 🌟 Key Features

### 🎮 Interactive 3D Stage (React Three Fiber)
- Custom open-air sunset stage with realistic props  
- Dynamic spotlights tracking the active speaker  
- Ambient lighting + reflective stage floor  
- Animated Droid characters (idle, blink, react, head-bob)  
- Free 360° camera rotation (mouse/touch)

---

### 🗣️ Voice-First AI Architecture
- **Real-Time ASR:** AssemblyAI speech-to-text  
- **Hinglish AI Persona:** Driven by Gemini 1.5 Flash  
- **Ultra-Low Latency Murf TTS:** Indian accent + near-instant response  
- Smart subtitle system:
  - Hindi (Devanagari) for on-screen subtitles  
  - Hinglish (Roman) for TTS accuracy  

---

## 🧠 Intelligent Game Loop

The host guides you through **3 fixed improv rounds**:

1. **Aggressive Sabzi Wala**  
2. **Nakhrebaaz Auto Driver**  
3. **Confused Alien in Mumbai**

After each scene:
- Silence detection (1.5s)  
- Auto-applause  
- AI performance analysis (creativity, commitment, absurdity)  
- Host roasts/praises you in Hinglish  
- Full transcript + summary saved to `game_history.json`

---

## 🛠️ Tech Stack

| Component | Tech |
|----------|------|
| Frontend | Next.js 14, Tailwind CSS |
| 3D Engine | React Three Fiber, Drei, Three.js |
| AI Logic | Google Gemini 2.5 Flash |
| TTS | Murf Falcon Streaming |
| ASR | AssemblyAI |
| Icons | Lucide React |

---

## 🚀 Getting Started

### **Prerequisites**
- Node.js 18+  
- API Keys:
  - Murf AI  
  - Google Gemini  
  - AssemblyAI  

---

### **1. Clone the Repository**

```
git clone https://github.com/SyncWithRaj/IITB-MurfAI_Hack.git
cd IITB-MurfAI_Hack
```

## Install Dependencies
```
npm install
# or
yarn install
```

## Configure Environment Variables
Create .env.local:

```
# AssemblyAI (Speech-to-Text)
ASSEMBLYAI_API_KEY=your_assemblyai_key_here
ASSEMBLYAI_UPLOAD_URL=https://api.assemblyai.com/v2/upload
ASSEMBLYAI_TRANSCRIPT_URL=https://api.assemblyai.com/v2/transcript

# Google Gemini
GOOGLE_API_KEY=your_google_gemini_key_here

# Murf AI (Text-to-Speech)
MURF_API_KEY=your_murf_api_key_here
MURF_TTS_URL=https://global.api.murf.ai/v1/speech/stream

# Environment
NEXT_PUBLIC_APP_ENV=development
```

## Run the Development Server
```
npm run dev
```

Open:
http://localhost:3000

🎬 How to Play

1. Click START

2. Host introduces the show

3. When the Red Mic Icon lights up → start speaking

4. Perform the scenario (aggressive sabzi wala, alien, etc.)

5. Host roasts/praises you

6. At end of show public applause you
  
8. After 3 rounds → final summary + show ending

📂 Project Structure
```
├── app/
│   ├── api/
│   │   ├── generate/      # Game brain: Gemini logic + Murf TTS
│   │   ├── transcribe/    # ASR: AssemblyAI speech recognition
│   ├── page.jsx           # Main 3D scene + UI overlays
│   ├── layout.jsx         # Root layout
├── public/                # Static assets
├── scenarios.json         # Predefined 3 improv scenarios
├── game_history.json      # Saved transcripts & summaries
└── README.md
```

# 📜 License
MIT License — feel free to remix or experiment.

# ⭐ Acknowledgements
Built for the Murf Voice Agent Hackathon (10 Days Challenge).
Showcases real-time voice interaction + 3D immersive UI + AI creativity evaluation.
