# ai-memory

A lightweight, client-side demonstration that visualizes how a large language model's (LLM) context/window (memory) can affect responses. The demo animates two scenarios — one without context history and one with context history — to illustrate why past interactions matter for follow-up questions.

## Files
- `index.html` — The full demo (single-file HTML + CSS + JS). Open this in a browser to view the animation and interactive controls.

## Demo overview
The demo is a polished, animated visualization (Portuguese default) showing:
- Scenario 1: No context history — the LLM answers but later says it doesn't remember the user's earlier question.
- Scenario 2: With context history — the LLM retains prior messages via a "history block" and answers follow-up questions correctly.
- A context bar that fills as the demo progresses, representing the LLM's context window usage.
- Buttons to restart and pause/resume the animation, and a language selector (pt/en/es).

The animation uses a sequence of timed steps to reveal messages, history blocks and update the context bar. It includes translations for Portuguese (pt), English (en) and Spanish (es).

## How to run (locally)
1. Open the demo directly in your browser:
   - Double-click `index.html` or open it via `File → Open` in a browser.


## Controls & UI
- Language selector: swaps UI text between Portuguese, English, and Spanish. The UI text keys live in a `translations` object.
- 🔄 Reiniciar (Restart): resets the animation and clears shown elements.
- ⏸️ Pausar (Pause) / ▶️ Continuar (Continue): toggles pausing. When paused, timeouts are cleared and resumed with proper elapsed-time accounting.
- Context bar: visually fills to show context/memory usage; color changes based on percentage thresholds (>60%, >80%).
- Progress indicator: step dots show which animation step is active/completed.