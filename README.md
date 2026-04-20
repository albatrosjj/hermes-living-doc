# The Silence Between Thunder: A Living Documentary

**A Hermes Agent + Kimi Moonshot AI Hackathon Project**

## What Is This?

A fully AI-generated bilingual (EN/TR) scrollytelling documentary about lesser-known human stories from World War II. Every image, every map, every voice, every word was created by artificial intelligence — orchestrated entirely through the Hermes Agent framework.

## Experience It

Open `index.html` in any modern browser, scroll down, and immerse yourself.

**Features:**
- Bilingual content (English / Turkish) with instant language switcher
- Auto-play narration that follows your scroll position
- Vintage military maps for every theater of war
- Combatant flags and front information for each chapter
- Cinematic film grain, parallax, and scroll-reveal animations
- Artistic poetic epilogues closing each chapter
- Keyboard navigation (arrow keys) and chapter dot navigation

## How It Was Made

| Layer | Tool | AI Model |
|---|---|---|
| **Research & Script** | `web_search`, `web_extract` | Kimi K2.6 |
| **Photographs** | `image_generate` | FLUX (FAL.ai) |
| **Maps** | `image_generate` | FLUX (FAL.ai) |
| **Voice Narration** | `text_to_speech` | Edge TTS |
| **Assembly** | `write_file`, `patch` | Hermes Agent pipeline |

### Architecture

```
outline.json (bilingual story + prompts + combatants + maps)
      |
      v
generate.py  --->  image_generate()  --->  8 photographs + 8 maps
      |            text_to_speech()   --->  16 narrated tracks (EN/TR)
      v
template.html (scrollytelling engine with language switcher)
      |
      v
  index.html  (single-file bilingual documentary)
```

## Chapters

1. **The Phoney War / Sahte Savaş** — Western Front — Sep 1939
2. **The Sands of Dunkirk / Dunkirk Kumları** — Dunkirk Evacuation — May 1940
3. **The Blitz / Blitz** — Home Front — Sep 1940
4. **Stalingrad / Stalingrad** — Eastern Front — Aug 1942
5. **The Unbreakable Tongue / Kırılamayan Dil** — Pacific Theater — 1942-45
6. **The White Rose / Beyaz Gül** — Internal Resistance — 1942-43
7. **Liberation and Its Weight / Kurtuluş ve Ağırlığı** — Allied Advance — 1944-45
8. **The Shadows Remain / Gölgeler Kalır** — Atomic Warfare — Aug 1945

## File Structure

```
.
├── index.html    # The documentary (self-contained)
├── images/       # 8 AI-generated photographs
├── maps/         # 8 AI-generated theater maps
└── audio/        # 16 AI-narrated voice tracks (EN + TR)
```

## Run Locally

No server required. Simply open `index.html` in a browser.

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Credits

- Built with [Hermes Agent](https://github.com/NousResearch/hermes-agent) by NousResearch
- Images & maps generated via [FAL.ai](https://fal.ai) FLUX model
- Narration powered by Kimi Moonshot AI + Edge TTS
- Created for the **Hermes Agent Creative Hackathon** (April 2026)

---

*This project contains no real archival footage or photographs. All visual and audio media is synthetic, generated to evoke historical atmosphere rather than document specific events.*
