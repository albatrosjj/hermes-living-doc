# The Silence Between Thunder: A Living Documentary

**A Hermes Agent + Kimi Moonshot AI Hackathon Project**

## What Is This?

A fully AI-generated scrollytelling documentary about lesser-known human stories from World War II. Every image, every voice, every word of narration was created by artificial intelligence — orchestrated entirely through the Hermes Agent framework.

## Experience It

Open `index.html` in any modern browser, scroll down, and immerse yourself. Audio narration auto-plays as you enter each chapter. Use arrow keys for keyboard navigation.

## How It Was Made

| Layer | Tool | AI Model |
|---|---|---|
| **Research & Script** | `web_search`, `web_extract` | Kimi K2.6 |
| **Images** | `image_generate` | FLUX (FAL.ai) |
| **Voice Narration** | `text_to_speech` | Edge TTS |
| **Assembly** | `write_file`, `patch` | Hermes Agent pipeline |

### Architecture

```
outline.json (story + prompts)
      |
      v
generate.py  --->  image_generate()  --->  8 unique AI images
      |            text_to_speech()   --->  8 narrated audio tracks
      v
template.html (scrollytelling engine)
      |
      v
  index.html  (single-file documentary)
```

## Chapters

1. **The Phoney War** — September 1939: The silence before the storm
2. **The Sands of Dunkirk** — May 1940: Civilian boats under fire
3. **The Blitz: Life Underground** — 1940-41: Singing beneath the bombs
4. **Stalingrad: The Frozen Hell** — 1942-43: Minus forty degrees
5. **The Unbreakable Tongue** — 1942-45: Navajo Code Talkers
6. **The White Rose** — 1942-43: Sophie Scholl's resistance
7. **Liberation and Its Weight** — 1944-45: The price of freedom
8. **The Shadows Remain** — August 1945: Hiroshima's eternal echo

## Creative Approach

Rather than a traditional documentary, this is a **living document**: an autonomous pipeline where the agent researches, writes, illustrates, narrates, and assembles a cinematic experience from a single theme prompt. The "creative" aspect is not just the output — it's the *process* itself: an AI agent acting as director, screenwriter, cinematographer, and sound designer.

## File Structure

```
.
├── index.html    # The documentary (self-contained)
├── images/       # 8 AI-generated photographs
└── audio/        # 8 AI-narrated voice tracks
```

## Run Locally

No server required. Simply open `index.html` in a browser.

```bash
cd deploy/
python3 -m http.server 8080
# open http://localhost:8080
```

## Credits

- Built with [Hermes Agent](https://github.com/NousResearch/hermes-agent) by NousResearch
- Images generated via [FAL.ai](https://fal.ai) FLUX model
- Narration powered by Kimi Moonshot AI + Edge TTS
- Created for the **Hermes Agent Creative Hackathon** (April 2026)

---

*This project contains no real archival footage or photographs. All visual and audio media is synthetic, generated to evoke historical atmosphere rather than document specific events.*
