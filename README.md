# Hanzi Steps

A from-zero Mandarin course in a single web page: 10 lessons with audio and quizzes, a tone trainer, spaced-repetition review a Claude-powered Coach tab with six study methods, and a searchable word list. The Coach talks to Claude only inside claude.ai; elsewhere it gives you a ready-made prompt to paste into Claude.

Open `index.html` in a browser. `app.html` is the same page without the document wrapper (used for the published Artifact).

Audio uses your device's built-in Chinese text-to-speech voice. Progress is saved in your browser.

## Using your own Ollama model for the Coach

1. Install [Ollama](https://ollama.com) and pull a model that is good at Chinese: `ollama pull qwen3`
2. In this folder run `python3 -m http.server 8000` and open http://localhost:8000
3. Open the Coach tab, choose **Ollama (your computer)** and press **Connect**.

Double-clicking `index.html` usually gets blocked by Ollama's browser security; serve it as above, or start Ollama with `OLLAMA_ORIGINS="*"`. The claude.ai-hosted version can't reach Ollama.
