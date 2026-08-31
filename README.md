# OmniVoice 2 GitHub Pages frontend

This static frontend is always available from GitHub Pages. It routes TTS requests as follows:

- up to 90 counted characters: Tailscale LOCAL first, then Modal on timeout/error;
- more than 90 counted characters: Modal directly.

The selected voice (`vasilije` or `zeljko`) is preserved across LOCAL and Modal fallback.

No API key, model file, reference audio, or private credential is included in this folder.
