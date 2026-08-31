# OmniVoice 2 GitHub Pages frontend

This static frontend is always available from GitHub Pages. It routes TTS requests as follows:

- up to 90 counted characters: Tailscale LOCAL first, then Modal on timeout/error;
- more than 90 counted characters: Modal directly.

The selected voice (`voice1` or `voice2`) is preserved across LOCAL and Modal fallback. The dedicated STOP button aborts the browser request and signals the active LOCAL or Modal worker to cancel; a stopped response is discarded and never added to the WAV library.

Settings also contains a persisted routing mode: `AUTO` keeps the 90-character LOCAL/Modal rule, while `SAMO MODAL` sends every request directly to Modal. The choice is stored in the browser and restored when the app is opened again.

No API key, model file, reference audio, or private credential is included in this folder.
