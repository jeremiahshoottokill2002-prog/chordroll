# ChordRoll 🎹

**106 chord progressions · 24 genres · drawn like an FL Studio piano roll · works offline.**

Pick a progression, change the key, hit play, then copy the notes straight into FL Studio, Cubase, or any DAW. Green bars = chord tones, teal bar = bass note, one chord per bar.

## What's inside

**Genres:** Classics 1958 · Afrobeats · Amapiano · Dancehall · Reggae · Hip Hop · Trap · Drill · R&B/Soul · Neo-Soul · Gospel · Pop · Smooth Rock · Rock · EDM/House · Jazz · Lo-fi · Blues · Country · Latin/Reggaeton · Cinematic · Highlife · Funk · Afro House

**Mood filters:** Happy · Sad · Chill · Dark · Euphoric · Romantic · Hype · Groovy · Nostalgic · Epic · Uplifting · Dreamy

Plus: transpose to all 12 keys, built-in playback with BPM + loop, and full 12-bar blues forms.

## Files

| File | What it does |
|---|---|
| `index.html` | The whole app (UI, data, audio engine) |
| `sw.js` | Service worker — caches everything so it runs with no internet |
| `manifest.webmanifest` | Lets phones install it as a real app |
| `icon-192.png`, `icon-512.png` | App icons |

## Put it on GitHub (2 minutes)

1. Create a new repo → **Add file → Upload files** → upload all 6 files
2. **Settings → Pages → Source: Deploy from a branch → main / (root)** → Save
3. Live at `https://YOURNAME.github.io/REPO-NAME/`

## Make it an offline app on your phone

1. Open your GitHub Pages link **once** in Chrome on your phone
2. Tap **⋮ → Add to Home screen → Install**
3. Done — it now opens full-screen like any app and works in airplane mode. The service worker caches everything on first visit.

> Note: the service worker needs HTTPS, which GitHub Pages gives you for free. Opening `index.html` directly from local storage still works for everything except the install/offline part.

## Add your own progressions

Open `index.html`, find the `PROGS` array, copy any entry:

```js
{name:'My Progression', genre:'Afrobeats', moods:['Groovy','Dark'],
 steps:[[0,'m','i'],[8,'','VI'],[3,'','III'],[10,'','VII']]}
```

Each step = `[semitones above the key root, chord quality, label]`.
Qualities: `'' m 7 maj7 m7 6 m6 dim dim7 m7b5 sus4 sus2 add9 madd9 9 maj9 m9 aug`.
There are infinite chord combinations in music — this library covers the patterns each genre actually runs on, and this is how you grow it.

## Roadmap

- [ ] MIDI export (.mid download of the selected progression)
- [ ] Inversions / voicing options
- [ ] Rhythm patterns (skank, dembow, log-drum stabs) instead of whole notes
- [ ] APK via Capacitor (wraps this exact HTML)

## Credits

Classic turnarounds adapted from *1500 Chord Progressions* by Walter Stuart (New Sounds in Modern Music, 1958). Genre progressions curated by ear.
