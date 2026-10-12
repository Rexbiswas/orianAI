# 🌌 ORIAN AI (OrionAI v2.0)
### *Next-Generation Autonomous AI Operating System, Digital Brain & Hardware Intelligence Dashboard*

[![Version](https://img.shields.io/badge/version-2.0.1-cyan.svg?style=for-the-badge)](package.json)
[![Architecture](https://img.shields.io/badge/Architecture-Digital%20Brain%20%2B%206%20Agents-blueviolet.svg?style=for-the-badge)](Orian_AI_Brain_Architecture.md)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Android%20%7C%20Electron%20%7C%20Web-00E5FF.svg?style=for-the-badge)](package.json)
[![Security](https://img.shields.io/badge/Security-HMAC--SHA256%20%7C%20Zero--Surveillance-brightgreen.svg?style=for-the-badge)](SECURITY_ARCHITECTURE.md)
[![License](https://img.shields.io/badge/License-Proprietary-red.svg?style=for-the-badge)](#)

---

## 📖 Table of Contents
1. [Overview](#-overview)
2. [Core Architecture & Digital Brain](#-core-architecture--digital-brain)
3. [Key Features & Capabilities](#-key-features--capabilities)
   - [Humanoid Perception & Sensory HUD](#1-humanoid-perception--sensory-hud)
   - [Autonomous 6-Agent Ecosystem](#2-autonomous-6-agent-ecosystem)
   - [Secure Windows Laptop Protection & Policy Engine](#3-secure-windows-laptop-protection--policy-engine)
   - [IoT & Hardware Robotics Subsystem (ESP32)](#4-iot--hardware-robotics-subsystem-esp32)
   - [Universal Execution & Self-Programming Engine](#5-universal-execution--self-programming-engine)
4. [Multi-Tier Memory & Database Pipeline](#-multi-tier-memory--database-pipeline)
5. [Tech Stack](#-tech-stack)
6. [Repository Structure](#-repository-structure)
7. [Installation & Setup](#-installation--setup)
   - [Prerequisites](#prerequisites)
   - [Environment Configuration](#environment-configuration)
   - [Running the Complete Stack](#running-the-complete-stack)
   - [Connecting Mobile Devices (Wi-Fi / Hotspot)](#connecting-mobile-devices-wi-fi--hotspot)
8. [Automated Verification & Testing](#-automated-verification--testing)
9. [Security, Privacy & Zero-Surveillance Standard](#-security-privacy--zero-surveillance-standard)
10. [REST API & WebSocket Endpoints](#-rest-api--websocket-endpoints)
11. [Author & Credits](#-author--credits)

---

## 🌟 Overview

**Orian AI** (OrionAI) is an enterprise-grade, biomimetic artificial intelligence platform designed to function as an autonomous digital brain rather than a standard conversational bot. Combining real-time human sensory awareness (facial expression analysis, gaze tracking, bidirectional speech), deep operating system orchestration, an HMAC-secured hardware/laptop protection engine, and hardware IoT robotics control, Orian AI unifies human-machine interaction into a single cohesive cybernetic dashboard.

```
                            ┌────────────────────────────────┐
                            │      ORIAN DIGITAL BRAIN       │
                            │   Cerebrum · Cerebellum · Core │
                            └───────────────┬────────────────┘
                                            │
         ┌──────────────────────────────────┼──────────────────────────────────┐
         ▼                                  ▼                                  ▼
┌─────────────────┐                ┌─────────────────┐                ┌─────────────────┐
│ PERCEPTION HUD  │                │ LAPTOP SECURITY │                │  IoT & ROBOTICS │
│ FaceMesh & Senses│               │ Zero-Surveillance│               │ ESP32 Telemetry │
│ ElevenLabs Voice│                │ Win32 Sleep Gate│                │ MQTT Subsystem  │
└─────────────────┘                └─────────────────┘                └─────────────────┘
```

---

## 🧠 Core Architecture & Digital Brain

Orian AI models human neuroanatomy to separate perception, cognitive reasoning, habitual execution, autonomic regulation, and defensive reflexes:

```
                            ORIAN BRAIN
                                 │
 ┌──────────────────────────────┼──────────────────────────────┐
 │                              │                              │
 ▼                              ▼                              ▼
Perception Brain          Memory Brain                 Reasoning Brain
(Eyes / Ears / Senses)    (Hippocampus)                (Prefrontal Cortex / LLM)
 • Real-time Video Stream  • Working Memory (Redis)     • Intent Classification
 • MediaPipe FaceMesh      • Long-term Vectors (Qdrant) • Multi-step Task Planner
 • ElevenLabs TTS & STT    • System DB (SQLite)         • Code Logic & Problem Solving
 │                              │                              │
 └──────────────────────────────┼──────────────────────────────┘
                                │
                                ▼
                     Executive Brain (Motor Cortex)
                     Execute Actions & Control System
    • Windows Native App Discovery & Launch (`app_resolver.py`)
    • Process Monitoring & Termination
    • File Operations & Temp Cleanup (`system_cleanup.py`)
    • Dynamic Tool Routing (`tool_router.py`)
                                │
                                ▼
                     Learning Brain (Cerebellum)
    • Autonomous Codebase Self-Diagnostics (`self_diagnostic.py`)
    • Self-Programming with AST Validation & Rollback Snapshots
    • Adaptive User Habits & Feedback Loop
```

### Neuroanatomical Subsystems
- **Cerebrum (`backend/features/brain/cerebrum.py`)**: High-level deliberate reasoning, multi-turn LLM reasoning, code synthesis, and strategic planning.
- **Cerebellum (`backend/features/brain/cerebellum.py`)**: Motor execution, automated routines, habitual task triggering, and lightning-fast low-latency actions.
- **Brainstem (`backend/features/brain/brainstem.py`)**: Core autonomic daemon monitoring host CPU, RAM, disk, network vital signs, and system heartbeat.
- **Amygdala / Protection Engine (`backend/features/protection/`)**: Threat, risk, and policy evaluator responsible for laptop defense, focus integrity, and immediate emergency response.

---

## ✨ Key Features & Capabilities

### 1. Humanoid Perception & Sensory HUD
- **3D Cybernetic HUD**: Built with Three.js (`@react-three/fiber`, `@react-three/drei`), Framer Motion, and Tailwind CSS.
- **Real-Time Facial & Emotional Vision**: Client-side MediaPipe FaceMesh integration detecting user engagement, head azimuth, spatial distance, and emotional state (Joy, Focus, Fatigue, Surprise, Neutral).
- **Audio Synthesizer & Speech Recognition**: Ultra-low latency voice interaction powered by ElevenLabs API and Web Speech synthesis, with real-time audio waveform visualizers.
- **Agent Presence Sync**: Live online greetings and telemetry broadcast across active cores.

### 2. Autonomous 6-Agent Ecosystem
Orian AI coordinates six specialized sub-agents orchestrated by `agent_orchestrator.py`:
1. **Perception Agent**: Ingests vision, audio input, active window metadata, OCR, and sensory events.
2. **Memory Agent**: Performs semantic recall and context storage across SQLite, Redis, and Qdrant.
3. **Reasoning Agent**: Leverages local/remote LLM models (OpenAI GPT-4o, Hugging Face Llama-2/Mistral, or Local Ollama) for decision synthesis.
4. **Developer Agent**: Code generation, unit test creation, refactoring, code linting, and automated syntax validation.
5. **Automation Agent**: Native Windows desktop actions, browser manipulation, file system modifications, and workflow automation.
6. **Learning & Security Agent**: Continuous self-monitoring, safety policy compliance, threat mitigation, and adaptive behavioral optimization.

### 3. Secure Windows Laptop Protection & Policy Engine
*Designed for complete laptop physical/operational protection with zero surveillance:*
- **Zero-Surveillance Standard**: Strictly collects only foreground window process names and sanitized window titles. **Never captures keystrokes, audio, webcam frames, clipboard data, or screen pixels.**
- **Deterministic Policy Engine**: Contextual protection modes (`WORK`, `STUDY`, `REST`, `OFF`). Restricts gaming, unapproved entertainment, system tampering, or unauthorized software during scheduled focus sessions.
- **Dynamic Risk Evaluation**: Real-time scoring (`LOW`, `MEDIUM`, `HIGH`, `CRITICAL`).
- **Graceful Escalation & Sleep Action**: Emits a 10-second audiovisual grace warning; if unaddressed, executes native Windows hibernation/sleep via controlled Win32 API (`PowrProf.SetSuspendState`).
- **Cryptographic Command Gateway**: Prevents command replay attacks via HMAC-SHA256 signatures, single-use UUID nonces, and 15-second TTL expiration.
- **Real-Time Mobile Push Alerts**: Streams live incident reports and one-tap owner override actions over WebSockets (`/ws/protection`).

### 4. IoT & Hardware Robotics Subsystem (ESP32)
- **Dedicated Firmware**: Complete ESP32 Arduino C++ firmware located in `firmware/esp32/orian_esp32.ino`.
- **Bidirectional Telemetry**: Real-time sensor readings (temperature, humidity, motion, proximity, voltage) streamed over MQTT (`1883`) or REST.
- **Actuator & Relay Control**: Command servo joints, lighting relays, buzzer alarms, and robotic peripherals directly from the Orian AI dashboard.
- **Automated Health Checks**: Continuous ping and heartbeat evaluation in `backend/features/iot/health_check.py`.

### 5. Universal Execution & Self-Programming Engine
- **Intent Detection Engine**: Automatically classifies commands into desktop execution, math calculation, system maintenance, diagnostic, or programming tasks.
- **Dual Math Engine**: High-speed AST parsing for arithmetic and SymPy symbolic mathematics for advanced calculus, limits, algebra, and physics expressions.
- **System Maintenance Tool**: Cleans temporary files, cache debris, and recycled memory to optimize machine performance.
- **Self-Programming Subsystem**: Safely analyzes, refactors, and patches its own codebase:
  - Generates rollback backup snapshots before modifying files.
  - Verifies code integrity with Python AST parsing.
  - Requires explicit owner authorization for self-modifications.

---

## 🗄️ Multi-Tier Memory & Database Pipeline

| Storage Layer | Technology | Primary Function |
| :--- | :--- | :--- |
| **Relational Storage** | **SQLite** (`orian_core.db`) | User profiles, task logs, system telemetry, paired device lists, policies, and configuration. |
| **Working Memory** | **Redis** | Active multi-turn conversation context, active agent states, temporary scratchpads, and live caches. |
| **Vector Semantic Memory** | **Qdrant** | Long-term memory embeddings, knowledge retrieval (RAG), learned developer patterns, and indexed documents. |
| **Physical File Vault** | **Local Disk** (`orian_storage/`) | Code artifacts, backup snapshots, audio logs, media files, and system diagnostics. |

---

## 💻 Tech Stack

### Frontend & UI
- **Frameworks:** Next.js 16 (App Router) + React 19 + Vite 6
- **Styling & Motion:** Tailwind CSS v4, Framer Motion, GSAP, Lucide Icons
- **3D & Graphics:** Three.js, React Three Fiber (`@react-three/fiber`), Drei (`@react-three/drei`)
- **Computer Vision:** Google MediaPipe (`@mediapipe/face_mesh`, `@mediapipe/camera_utils`)
- **Voice & Speech:** ElevenLabs SDK (`@elevenlabs/elevenlabs-js`), Web Audio API, Custom Audio Recorder
- **State & Networking:** Zustand, Axios, Socket.IO Client

### Backend & AI Intelligence Core
- **Framework:** Python 3.11+ / FastAPI, Uvicorn, Pydantic v2
- **Agent Framework:** Custom biomimetic agent orchestrator (`Cerebrum`, `Cerebellum`, `Brainstem`)
- **Symbolic & Math Tools:** SymPy, Python AST Engine
- **System Integration:** Windows Win32 API (`ctypes`, `win32gui`, `win32process`, `psutil`)
- **Security:** HMAC-SHA256, AES-256-GCM, Cryptographic Nonce & Replay Gateway

### Multi-Platform & Infrastructure
- **Desktop Packaging:** Electron 41 + Electron Builder (Windows NSIS / Mac / Linux)
- **Mobile Packaging:** Capacitor 8 (`@capacitor/android`, `@capacitor/core`)
- **IoT Firmware:** C++ / Arduino for ESP32 with MQTT (PubSubClient) & WiFiClientSecure
- **Proxy Server:** Node.js Express server + HackerAI local security bridge

---

## 📂 Repository Structure

```text
orionAI/
├── android/                         # Android Studio / Capacitor mobile project
│   ├── app/                         # Native Android source code & manifests
│   └── build.gradle                 # Gradle build scripts
├── backend/                         # Python FastAPI Intelligence Core
│   ├── agents/                      # Standalone AI agent modules
│   ├── brain/                       # Brain management & cognitive structures
│   ├── features/                    # Modular feature subsystems
│   │   ├── agents/                  # 6 Autonomous agents (Perception, Developer, etc.)
│   │   ├── brain/                   # Cerebrum, Cerebellum, Brainstem, Memory DB
│   │   ├── execution/               # App resolver & Windows desktop executor
│   │   ├── iot/                     # IoT manager, MQTT broker, health checker
│   │   ├── neural/                  # Self-diagnostics & self-programmer
│   │   ├── planner/                 # Intent detector & real-world reasoner
│   │   ├── protection/              # Activity monitor, policy engine, Win32 sleep
│   │   ├── security/                # Cryptographic authentication & token gateway
│   │   └── tools/                   # Math engine, system cleanup, tool router
│   ├── tests/                       # Unit tests & verification suites
│   ├── config.py                    # Environment & path configuration
│   ├── main.py                      # FastAPI app entry point & routes
│   └── requirements.txt             # Python dependencies
├── firmware/                        # Hardware & robotics code
│   └── esp32/
│       └── orian_esp32.ino          # ESP32 C++ firmware (Sensors, Actuators, MQTT)
├── orian_storage/                   # Local persistent storage vault
│   ├── documents/                   # Documents indexed for vector search
│   ├── generated/                   # Autonomous code & asset generation
│   ├── logs/                        # System event & execution logs
│   ├── orian_core.db                # Primary SQLite database
│   └── projects/                    # Agent project workspaces
├── public/                          # Public static assets & icons
├── server/                          # Node.js backend proxy server
│   ├── index.js                     # Express API & proxy routes
│   └── package.json                 # Node dependencies
├── src/                             # Next.js / Vite React frontend
│   ├── app/                         # Next.js application routes
│   ├── components/                  # Reusable HUD & cybernetic UI widgets
│   ├── context/                     # LogContext, VoiceContext, AuthContext
│   ├── features/                    # Frontend feature implementations
│   │   ├── brain/                   # AICore, NeuralSchema, CircularCore
│   │   ├── chat/                    # VoiceInput, TextCommand, ChatPanel
│   │   ├── iot/                     # IoTModalDashboard, telemetry charts
│   │   ├── protection/              # ProtectionDashboard, paired devices
│   │   ├── senses/                  # MediaPipe EmotionDetection, gaze tracking
│   │   └── tasks/                   # LiveTaskDashboard, MemoryTimeline
│   ├── layouts/                     # Master HUD layout (FirstPageLayout.jsx)
│   ├── utils/                       # Voice synthesizer, audio recorder, sound FX
│   └── config.js                    # Frontend endpoint configuration
├── main.cjs                         # Electron desktop main process
├── preload.cjs                      # Electron context bridge & IPC security
├── start-all.ps1                    # One-click PowerShell full-stack launch script
├── package.json                     # Root npm package scripts & dependencies
└── README.md                        # Project documentation (this file)
```

---

## 🚀 Installation & Setup

### Prerequisites
- **Operating System:** Windows 10/11 (for native Win32 app resolution & power control), Linux, or macOS
- **Node.js:** v18.0.0 or higher
- **Python:** v3.10 to v3.14
- **Git**

---

### Environment Configuration

1. Copy `.env.example` to `.env`:
   ```powershell
   Copy-Item .env.example .env
   ```
2. Configure your secret keys inside `.env`:
   ```ini
   # Master Security Keys
   ORIAN_SECRET_KEY=generate_a_random_64_char_hex_string
   ORIAN_ENCRYPTION_KEY=generate_a_random_64_char_hex_string

   # Server Settings
   HOST=0.0.0.0
   PORT=8000
   DEBUG=true

   # LLM Providers (Optional for cloud models)
   DEFAULT_PROVIDER=local
   OPENAI_API_KEY=your_openai_key_here
   HUGGINGFACE_API_KEY=your_hf_key_here

   # ElevenLabs Voice Synthesis (Optional)
   VITE_ELEVENLABS_API_KEY=your_elevenlabs_api_key
   VITE_ELEVENLABS_VOICE_ID=your_elevenlabs_voice_id
   ```

---

### Running the Complete Stack

#### Option A: One-Click PowerShell Launcher (Recommended)
Launch the FastAPI Intelligence Core, Node.js Proxy, HackerAI Security Bridge, and Vite Frontend simultaneously:
```powershell
.\start-all.ps1
```

#### Option B: Manual Process Launch

1. **Start the Python Intelligence Core (Backend):**
   ```powershell
   cd backend
   pip install -r requirements.txt
   python main.py
   ```
   *Backend will start on `http://localhost:8000` (docs available at `/docs`).*

2. **Start the Node.js Server:**
   ```powershell
   cd server
   npm install
   npm run dev
   ```
   *Node server will start on `http://localhost:5000`.*

3. **Start the Frontend Dashboard:**
   ```powershell
   # In the root project directory:
   npm install
   npm run dev:vite
   ```
   *Frontend will launch at `http://localhost:5173`.*

4. **Launch as Electron Desktop App (Optional):**
   ```powershell
   npm run electron:dev
   ```

---

### Connecting Mobile Devices (Wi-Fi / Hotspot)

To receive real-time push alerts and approve override commands on your smartphone:
1. Ensure your laptop and phone are on the **same Wi-Fi network** (or connect laptop to your phone's **Mobile Hotspot**).
2. Obtain your laptop's IPv4 address by running `ipconfig` in PowerShell (e.g. `192.168.1.15`).
3. Open Chrome or Safari on your phone and navigate to:
   ```
   http://192.168.1.15:5173
   ```
4. Click the **Shield Icon (🛡️)** on the laptop dashboard > navigate to **`PAIRED DEVICES`** > create a pairing code > tap **`APPROVE`** on your device to establish an encrypted WebSocket channel.

---

## 🧪 Automated Verification & Testing

Orian AI includes a test suite verifying intent detection, Win32 application resolution, system cleanup, mathematical engines, self-diagnostics, and tool routing:

```powershell
python backend/tests/test_orion_upgrade.py
```

### Test Suite Coverage:
- `test_01_intent_detection`: Validates 6 intent categories (Desktop actions, math, maintenance, etc.).
- `test_02_desktop_software_control`: Verifies dynamic resolution, launch, and termination of Windows processes.
- `test_03_system_cleanup`: Tests safe discovery and cleanup of system temporary caches.
- `test_04_mathematics_engine`: Validates AST evaluation and SymPy symbolic calculus (`derivative of x^2`).
- `test_05_real_world_reasoning`: Tests multi-step analytical problem solving.
- `test_06_self_diagnostics`: Validates automated subsystem health scoring.
- `test_07_self_programming`: Tests code inspection, AST syntax validation, and rollback backup snapshot generation.
- `test_08_tool_router_end_to_end`: Tests seamless end-to-end user query execution.

---

## 🔒 Security, Privacy & Zero-Surveillance Standard

Orian AI is engineered to protect user privacy without compromising security:

```
[ Active Window Tracker ] ───► Sanitizes Title & Process Name Only
                                 │
                                 ├──► NO Keylogging / Keystroke capture
                                 ├──► NO Screen recordings or screenshots
                                 ├──► NO Webcam or audio eavesdropping
                                 └──► NO Personal message scraping
```

- **HMAC Command Signatures**: Every action command (e.g. system sleep, app closure) must include an `HMAC-SHA256` token generated using `ORIAN_SECRET_KEY`.
- **Replay Protection**: Timestamps are validated with a 15-second TTL window; single-use nonces prevent packet injection.
- **Developer Whitelist**: VS Code, JetBrains IDEs, Python, Node, Git, Terminals, and designated security testbeds are permanently whitelisted and bypass restrictions.
- **Rollback Snapshots**: Any modification made by the self-programming engine automatically generates a restore point before applying patches.

---

## 🌐 REST API & WebSocket Endpoints

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/` | System health and online status check |
| `POST` | `/api/chat` | Main conversational query & agent dispatch |
| `GET` | `/api/protection/status` | Current laptop protection status & active focus mode |
| `POST` | `/api/protection/focus-mode` | Set focus mode (`WORK`, `STUDY`, `REST`, `OFF`) |
| `POST` | `/api/protection/action` | Execute controlled laptop action (sleep, lock, dismiss) |
| `GET` | `/api/protection/devices` | List registered and paired mobile devices |
| `POST` | `/api/protection/devices/pair` | Initiate cryptographic device pairing |
| `GET` | `/api/iot/devices` | Enumerate registered IoT sensors and microcontrollers |
| `POST` | `/api/iot/command` | Send command to ESP32 actuators / relays |
| `WS` | `/ws/protection` | Real-time WebSocket channel for mobile risk alerts |
| `WS` | `/ws/telemetry` | Real-time system telemetry and IoT data stream |

---

## 👨‍💻 Author & Credits

- **Developer:** Rishi Biswas ([@Rexbiswas](https://github.com/Rexbiswas))
- **Project:** OrionAI / Orian Digital Brain v2.0
- **Architecture:** Humanoid Biomimetic AI, Autonomous Agents & Windows Zero-Surveillance Defense

---

<p align="center">
  <i>Developed for autonomous desktop mastery, privacy-first system defense, and modern human-AI collaboration.</i>
</p>
