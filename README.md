# HSK 2 Flashcards

A browser-based flashcard app to study all New HSK 3.0 Level 2 Chinese vocabulary words (~200 words).

## Features

- **~200 HSK 2 words** (New HSK 3.0 standard) — Chinese characters, pinyin, English meaning, and an example sentence
- **Stroke order animations** — animated GIF showing how to write each character
- **Pronunciation audio** — auto-plays the Chinese word when a new card appears; replay with 🔊
- **Flip animation** — tap the card (or press `Space`) to reveal the answer
- **Track progress** — mark each word as ✅ Know or 🔄 Review again
- **Study again mode** — focus only on words you marked for review
- **Word list** — searchable table of all words with their status
- **Progress saved** — stored in browser localStorage, survives page refreshes
- **Reset progress** — one-tap reset button in the UI (no DevTools needed)
- **Keyboard shortcuts** — `Space`/`F` to flip, `←`/`→` to navigate, `1` = review, `2` = know

## How to Run

No installation needed — it's a single HTML file.

**Option 1: Open directly in browser**
```
open index.html
```

**Option 2: Serve locally with Python**
```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## How to Study

1. Cards are shuffled randomly each session
2. Listen to the pronunciation (auto-plays on each new card)
3. Tap the card (or press `Space`) to flip and see the meaning, stroke order, and example sentence
4. Mark **✅ I know it** if you're confident, or **🔄 Review again** if you need more practice
5. Switch to **Study again** mode to drill only the words you're unsure about
6. Use the **Word list** tab to search and see your overall progress

## Progress

Progress is saved automatically in your browser's localStorage — no account needed.  
To reset: tap the **🗑 Reset progress** button in the app.  
Or paste this in the browser console:
```js
localStorage.removeItem('hsk2-known'); localStorage.removeItem('hsk2-learn'); location.reload();
```

## Sources

- Vocabulary: [New HSK 3.0 (2025)](https://github.com/krmanik/HSK-3.0) word list
- Stroke order GIFs: [dictionary.writtenchinese.com](https://dictionary.writtenchinese.com)

## Tech

Plain HTML, CSS, and vanilla JavaScript — no build tools, no dependencies, no backend.  
Fonts: [Noto Sans SC](https://fonts.google.com/noto/specimen/Noto+Sans+SC) (Chinese) + [Inter](https://fonts.google.com/specimen/Inter) (UI).  
Audio: Web Speech API (built-in browser TTS, `zh-CN` voice).

## Related

- [hsk1-flashcards](https://github.com/marishachem/hsk1-flashcards) — HSK Level 1 (~300 words, red theme)
