# What Did I Miss? — Privacy-First Chat Catch-Up Micro-App

> **A 100% Client-Side, On-Device Chat Intelligence Dashboard**  
> *Zero Cloud APIs, Zero Network Telemetry, 100% Private.*

---

## 🚀 How to Run

### Option A: Instant Direct Browser Launch (No Terminal Needed)
1. Open your file explorer and navigate to: `c:\message manager`
2. **Double-click [`index.html`](file:///c:/message%20manager/index.html)** (or right-click → *Open with Google Chrome / Microsoft Edge / Firefox / Safari*).
3. The application runs immediately in your browser.

### Option B: Local Vite Development Server
```bash
# In c:\message manager
npm run dev
# Open http://localhost:5173/ in your browser
```

---

## 📄 Submission Documentation

The formal **Preliminary Design Report (PDR)** for hackathon submission is located at:
👉 **[`docs/PDR.md`](file:///c:/message%20manager/docs/PDR.md)**

It contains:
- Complete Abstract & Background
- System Architecture Diagram (Mermaid)
- Detailed Feature Implementation Status Matrix
- Algorithmic breakdown of parsing, NLP entity extraction, prioritization, and contradiction detection
- Privacy & Offline Security evaluation
- Verified test cases and future roadmap

---

## 🌟 Key Features

### 1. 100% On-Device Privacy & Security
- **Zero Cloud APIs:** All message tokenization, entity detection, mention matching, conflict spotting, and extractive summarization execute locally in browser memory.
- **Zero Telemetry / Zero Tracking:** No data or conversation content is ever transmitted over the network.
- **Inspectable:** Verify with Browser DevTools (F12) → Network Tab (0 requests).

### 2. Conversation Input & Formats
- **Paste & Analyze:** Paste chat logs in standard formats (WhatsApp iOS/Android exports, Telegram, Discord, Slack, or plain `Sender: message`).
- **Local File Import:** Direct local `.txt` / `.chat` file picker using the HTML5 `FileReader` API.
- **One-Click Demo Sample:** Built-in CS 490 Senior Capstone group chat demonstrating all features.

### 3. Rule-Based Deterministic NLP Engine
- **Direct & Alias Mentions:** Distinguishes between direct action requests (e.g. `@Alex we need your backend API docs by tomorrow 5 PM`) and passive mentions.
- **Action Items & Assignments:** Identifies tasks, responsible teammates (e.g. `Maya`, `Carlos`), and provides an interactive checklist to mark items complete or undo.
- **Deadlines & Ambiguity Flagging:** Extracts specific calendar deadlines (`Friday Oct 15 at 11:59 PM`, `Nov 3rd in Hall B`) while flagging ambiguous phrases (`sometime this week`).
- **Confirmed Decisions:** Detects agreed architecture resolutions (`PostgreSQL with JSONB over MongoDB`).
- **Contradiction Detection:** Spots conflicting information in the conversation stream (e.g. meeting room shifted from `Room 204` to `Room 318` due to maintenance).

### 4. Interactive Dashboard & Findings Center
- **Live Computed Metrics:** Real-time counts for Messages Analyzed, Important Findings, Personal Mentions, Open Tasks, and Upcoming Deadlines.
- **Categorized Filter Tabs:** Filter by *All*, *High Priority*, *Mentions*, *Tasks*, *Deadlines*, and *Decisions*.
- **Live Search & Urgency Sorting:** Instant search across titles, senders, and descriptions.
- **Traceability Inspector:** Click **"Inspect Context"** on any finding to view the exact target message highlighted alongside surrounding conversation lines.
- **Markdown Export:** Download a structured markdown summary report of your findings with one click.

---

## 📁 Project Structure

```
c:\message manager\
├── docs\
│   └── PDR.md         # Comprehensive Preliminary Design Report for submission
├── index.html         # Semantic HTML5 application structure with accessible components
├── style.css          # Vanilla CSS design system (clean light theme, navy/indigo accents)
├── script.js          # Pure JavaScript NLP parser, entity extractor, & UI state manager
├── package.json       # Project configuration & Vite dev server scripts
└── README.md          # Project overview, setup, and documentation index
```
