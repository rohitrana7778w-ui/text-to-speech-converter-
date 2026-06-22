# Voicebox — Text to Speech Converter

A simple, single-file web app that reads any text out loud using your browser's built-in voices. No installation, no API key, no server, and no data ever leaves your device.

## Files

| File | Description |
|---|---|
| `text-to-speech.html` | The complete app — HTML, CSS, and JavaScript all in one file |
| `README.md` | This file |

## How to Run It

1. Download `text-to-speech.html`.
2. Double-click it (or right-click → **Open with** → your browser).
3. That's it — the app opens directly in your browser.

No build step, no `npm install`, no internet connection required after the page loads (it only fetches Google Fonts online; if you're offline, it'll fall back to default fonts and still work fine).

## How to Use It

1. Type or paste any text into the text box.
2. Pick a **voice** from the dropdown (the list comes from your browser/OS — Chrome and Edge usually offer the most voices).
3. Adjust:
   - **Rate** — how fast it speaks (0.5× to 2×)
   - **Pitch** — how high or low the voice sounds
   - **Volume** — how loud it plays
4. Click **▶ Speak**.
5. Use **⏸ Pause / ▶ Resume** and **⏹ Stop** to control playback while it's reading.

A waveform animation pulses while the text is being read, and a live character count plus a rough time estimate is shown above the controls.

## How It Works

The app uses the browser's native **Web Speech API** (`SpeechSynthesisUtterance` / `speechSynthesis`), which is built into Chrome, Edge, Safari, and Firefox. Because the speech engine lives in your browser/OS, this means:

- ✅ Completely free, no API key needed
- ✅ Works offline once the page is open
- ✅ Nothing you type is uploaded or stored anywhere
- ⚠️ Available voices differ by browser and operating system

## Browser Support

Works best in the latest **Chrome**, **Edge**, or **Safari**. If your browser doesn't support speech synthesis, the app will show a message letting you know.

## Customizing

Everything is in one file (`text-to-speech.html`), so you can open it in any text editor (Notepad, VS Code, Sublime, etc.) to tweak:

- **Colors / fonts** — edit the `:root { ... }` CSS variables near the top of the `<style>` section
- **Default rate/pitch/volume** — edit the `value="..."` attributes on the sliders in the HTML
- **Behavior** — edit the JavaScript inside the `<script>` tag at the bottom

No frameworks or build tools are involved — it's plain HTML/CSS/JS.
