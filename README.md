# 🖥️ ArchiFlow Pro — CPU Pipeline Simulator

![HTML](https://img.shields.io/badge/HTML5-orange.svg)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow.svg)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-CDN-38bdf8.svg)
![Status](https://img.shields.io/badge/Status-Academic%20Project-brightgreen.svg)

An **interactive, animated visualization** of a non-pipelined CPU datapath, built as a **Computer Architecture** course project. Watch an instruction move step-by-step through the classic five stages — **Fetch, Decode, Execute, Memory, Writeback** — with a second, extended version that adds a working ALU and register file.

---

## 📋 Overview

Understanding how an instruction physically moves through a CPU's datapath is much easier to see than to read. ArchiFlow Pro animates a single instruction's journey through each pipeline stage one step at a time (or on autoplay), highlighting only the active hardware unit at each cycle — turning the textbook 5-stage pipeline diagram into something you can actually watch execute.

## ✨ Features

- 🎬 **Step-by-Step or Autoplay Execution** — advance one cycle at a time or let the simulation run automatically
- 🎯 **Isolated Hardware Highlighting** — only the currently active stage/unit lights up, dimming everything else for clarity
- 🧮 **Two Simulator Versions:**
  - `non-pipelined.html` — the base 5-stage non-pipelined datapath simulator
  - `non-pipelined-with-alu.html` — an extended version with a functional **ALU** and visible **register file** (`reg0`–`reg7`), showing actual arithmetic operations execute during the Execute stage
- 🔧 **Configurable Inputs** — set instruction count, clock speed, and custom instructions/values to simulate
- 📊 **Live Status & Timing Display** — cycle time, throughput, and current stage status shown in real time

## 🛠️ Tech Stack

| Category | Details |
|---|---|
| Structure | HTML5 (self-contained, inline styles & scripts) |
| Styling | Tailwind CSS (CDN) + custom CSS variables for stage color-coding |
| Icons/Fonts | Font Awesome, Google Fonts (Plus Jakarta Sans, Space Grotesk) |
| Logic | Vanilla JavaScript (ES6) |

## 📁 Project Structure

```
ArchiFlow-Pro-CPU-Pipeline-Simulator/
├── non-pipelined.html            # Base 5-stage non-pipelined datapath simulator
├── non-pipelined-with-alu.html   # Extended version with ALU + register file
└── README.md
```

## ▶️ How to Run

No build step or server required — everything runs client-side in the browser.

```bash
git clone https://github.com/<your-username>/ArchiFlow-Pro-CPU-Pipeline-Simulator.git
cd ArchiFlow-Pro-CPU-Pipeline-Simulator
open non-pipelined.html   # or non-pipelined-with-alu.html
```

Or try it live via GitHub Pages (see below).

<img width="1917" height="908" alt="image" src="https://github.com/user-attachments/assets/88cf2235-fd54-4472-b8ab-68d0343bc8d2" />


## 🌐 Live Demo (optional setup)

Since this is pure HTML/CSS/JS, you can host it for free with **GitHub Pages**:
1. Go to your repo → **Settings** → **Pages**
2. Under "Source," select the `main` branch and root folder
3. Save — your simulator will be live at:
   `https://<your-username>.github.io/ArchiFlow-Pro-CPU-Pipeline-Simulator/non-pipelined.html`

   <img width="1917" height="276" alt="image" src="https://github.com/user-attachments/assets/6a21ae77-9536-418b-80bd-ea377b1104c2" />


## 🕹️ Usage

1. Open either HTML file in a browser
2. Set the instruction count, clock speed, and/or custom instruction/value inputs
3. Click **Step** to advance one cycle at a time, or **Play** to autoplay the full instruction cycle
4. Watch the datapath diagram highlight the active hardware unit (Fetch → Decode → Execute → Memory → Writeback) as the instruction moves through
5. In the ALU version, observe register values (`reg0`–`reg7`) update live as arithmetic operations execute

## 📚 What I Learned

- Visualizing the classic 5-stage instruction cycle (IF-ID-EX-MEM-WB) as an animated, interactive diagram rather than a static textbook figure
- Implementing a simple ALU and register file model in JavaScript to simulate real arithmetic execution
- Managing sequential, timed UI state (step vs. autoplay modes) in vanilla JavaScript
- Using isolated highlighting/dimming to make a complex diagram easier to read at each step

## 🔮 Future Improvements

- Add a true pipelined mode (overlapping instructions across stages) for direct comparison against the non-pipelined version
- Support multiple simultaneous instructions with hazard detection (data/control hazards)
- Add a performance comparison chart (cycles, throughput) between pipelined and non-pipelined execution

## 🎓 Course

Computer Architecture — BS Computer Science

## 👩‍💻 Author

**Fatima Nadeem**
BS Computer Science

## 📎 Notes

- Requires an internet connection on first load (Tailwind CSS, Font Awesome, and Google Fonts are loaded via CDN)
- Tested in modern Chromium/Firefox browsers; no build tools or dependencies needed
