# Song to Minecraft Note Blocks

Drop any audio file (MP3, WAV, OGG, M4A, FLAC) and get a **.nbs** file ready to use in Minecraft via [Note Block Studio](https://noteblock.studio).

## How to use

1. Open `index.html` in your browser (Chrome / Firefox / Edge)
2. Drop your audio file onto the page
3. Adjust BPM, sensitivity, and instrument if needed
4. Click **Convert** and wait (30-90s for long songs)
5. Download the `.nbs` file
6. Open it in [OpenNoteBlockStudio](https://noteblock.studio) to preview and export to Minecraft

## Vanilla compatible

All notes are folded into the **25-note vanilla range** (F#3 to F#5).  
Notes outside this range are transposed up or down by octaves to fit.  
Up to **25 simultaneous notes** per tick are supported.

## How it works

- Web Audio API decodes the audio file in your browser
- An 8192-point FFT runs across overlapping frames to detect pitches
- Spectral peaks are tracked into note onset/offset events
- Notes are quantized to the nearest 16th-note tick at the detected BPM
- A valid NBS v5 binary file is assembled and offered for download

## No server, no install, no Python

Everything runs locally in your browser. Just open `index.html`.

## Host on GitHub Pages

1. Push this folder to a GitHub repository
2. Go to repo Settings > Pages > set source to `main` branch, `/ (root)`
3. Your converter is live at `https://yourusername.github.io/repo-name`
