# 🐣 Be Hoppy!
*A Sentient Pixel Companion for Joy, Awareness, and Flopsy Bunny*  
✨ Raspberry Pi • AI Tamagotchi • Pixel Art Display System

---

## 🌸 Overview

**Be Hoppy!** is a joyful, emotionally intelligent pixel system starring your AI-powered virtual companion: **Flopsy Bunny**.

Blending pastel animation, LED display hardware, AI personality, and storytelling, it’s both a **creative art installation** and an **interactive emotional interface**.

---

## 🧸 Meet Flopsy Bunny

Flopsy Bunny is your **pixel-based AI friend** who lives on a 64×64 matrix. Her expressions, energy, and needs are visualized through animation, side meters, and AI personality.

Flopsy reacts to system state, AI feedback, or user interactions in real time—just like a Tamagotchi, but smarter, cuter, and more connected.

---

## 🖥️ Hardware Display Layout

  [Btn1] [Btn2] [Btn3]

[ Health Panel ]    [ Manna Panel ]
8x8x4 MAX7219       8x8x4 MAX7219

   ┌──────────────┐
   │ Flopsy Bunny │ ← 64×64 RGB Matrix
   └──────────────┘

- 🩺 Left panel = **Health** (computed by `compute_health()`)  
- ✨ Right panel = **Manna** (emotional energy via `compute_manna()`)  
- 🎨 Center display shows Flopsy's AI-generated image and animation

---

## 🧬 Behavior Meta-Language

Each pet has a `.bhp` file (e.g., `flopsy.bhp`) that describes their mood, image, and current needs:

```yaml
name: Flopsy Bunny
image: flopsy_2024_04.png
mood: playful
energy: 83
focus: 72
ears: relaxed
tail: hop_slow
fitness:
  health: 91
  manna: 67

These values power animations, render states, and visual indicators.

⸻

🚀 App Launch Modes

Be Hoppy can launch in different modes via CLI or config:

Mode	Description
menu	Starts the web dashboard
rotation	Plays through pixel story scenes
scene:X	Loads a specific scene (e.g., scene:act3_scene2)
tamagotchi	Flopsy Bunny takes center stage

Example:

python3 run_display.py mode=tamagotchi

Or configure in config.json:

{
  "mode": "tamagotchi",
  "pet_file": "flopsy.bhp",
  "ai_mode": "cloud"
}



⸻

🎨 Features
	•	🧸 AI Tamagotchi Mode (Flopsy Bunny)
	•	📊 Real-time Health & Manna meters
	•	🧠 Fitness functions with emotional feedback
	•	🎭 Scene-based pixel animation (Acts 1–5)
	•	🖼️ Pixel art generation & animation engine
	•	🌐 Web UI for uploads and control
	•	☁️ Cloud or local AI personality
	•	🖱️ 3-button interactive interface
	•	💾 Local save + image reuse
	•	🧠 Emotion-reflective visual design

⸻

📁 Project Structure

be-hoppy/
├── scenes/              # Pre-scripted pixel animations
├── tamagotchi/          # Flopsy logic, fitness, rendering
├── matrix/              # Matrix + side LED control
├── generator/           # Art/animation generation engine
├── static/              # Uploaded/generated art
├── templates/           # Flask HTML UI
├── server.py            # Web server
├── run_display.py       # Main launcher
├── config.json          # Launch config
└── README.md



⸻

🤝 Part of the PenphinMind Ecosystem

Be Hoppy! is one branch of a larger system of cognition, expression, and joy:

🌊 PenphinMind

The dual-minded cognitive engine. Logic and intuition woven together to support emotional flow and adaptive thought.

📘 SeeingSharp

The narrative and scripting framework behind your scene logic, emotions, and animations. Used to generate story arcs and musical metaphors for Flopsy and beyond.

📊 RoverByte

Your AI-linked task and mood tracker. Feeds emotional data into Be Hoppy! and Flopsy for real-time display and feedback.

⸻

🌐 Web Interface

Once the system is running, visit:

http://<your-raspberry-pi-ip>:5000

There you can:
	•	🎬 Trigger scenes
	•	🐰 View or update Flopsy Bunny
	•	🖼️ Upload pixel art
	•	📤 Review saved animations

⸻

🌱 Why “Be Hoppy”?

It’s not just a pun — it’s a principle.

A reminder to live joyfully, bounce gently, and reflect in color.
Be Hoppy expresses joy through motion, emotion through pixels, and awareness through animation.

---
🤝 Part of the PenphinMind Ecosystem

Be Hoppy! is one branch of a larger system of cognition, expression, and joy:

## 🤝 Part of the PenphinMind Ecosystem

**Be Hoppy!** is one branch of a larger system of cognition, expression, and joy:

### 🌊 [PenphinMind](https://github.com/CodeMusic/PenphinMind)  
The dual-minded cognitive engine. Logic and intuition woven together to support emotional flow and adaptive thought.

### 📘 [SeeingSharp](https://SeeingSharp.ca)  
The narrative and scripting framework behind your scene logic, emotions, and animations. Used to generate story arcs and musical metaphors for Flopsy and beyond.

### 📊 [RoverByte](https://github.com/CodeMusic/RoverByte)  
Your AI-linked task and mood tracker. Feeds emotional data into Be Hoppy! and Flopsy for real-time display and feedback.
⸻

🧁 License

MIT License — hop freely, share widely. 🐰✨
