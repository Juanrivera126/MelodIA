# MelodIA

**Your intelligent songbook: create, save, and share songs with AI.**

MelodIA generates square album covers, lyrics, and songs from a genre, voice, and description or theme. Results can be downloaded as individual songs or as an interactive HTML grid.

## Features

- On-demand square cover generation.
- Fifteen visual styles, including vintage, 3D cartoon, anime, watercolor, and cyberpunk.
- Spanish and English language selection for the interface, lyrics, and song generation.
- Custom music genre through a dialog box.
- Music generation with `google/lyria-3-clip-preview` through Pollinations AI.
- Lyrics generation before audio generation; the lyrics are included in the prompt sent to Lyria.
- Pollinations AI as the only provider.
- Local persistence of the Pollinations AI API key.
- MP4 song downloads when the browser supports MP4 `MediaRecorder` output.
- HTML grid downloads with one card per generated song.
- One cover and one independent player per grid card.
- Editable lyrics below the cover for regenerating the MP4 with modified lyrics.
- Existing grids do not use one shared cover image; each video uses its own first frame.

## Main Files

- `index.html`: application for generating covers, lyrics, songs, and grids.
- `grilla.html`: generated HTML grid ready to open in a browser.
- `ejemplo.html`: image-grid example.
- `README.md`: Spanish documentation.
- `README.en.md`: English documentation.
- `README.html`: browser-readable documentation.
- `imagen.png`, `propiedades.png`, and `gifanimadoRedProyecto.gif`: visual project assets.
- `Bajo_la_luna_del_cafetal.mp4`: multimedia test asset.

## Usage

1. Open `index.html` in a modern browser.
2. Enter and validate your Pollinations AI API key.
3. Select the interface and song language.
4. Select a genre and voice. Choose **Custom** to enter a custom genre in a dialog box.
5. Write the song description or theme.
6. Select one of the fifteen visual styles.
7. Click **Generate New** to create the cover, lyrics, and audio.
8. Edit the lyrics below the cover and click **Regenerate with these lyrics** to create another version.
9. Click **Download song** to save the current MP4.
10. Click **Download grid** to generate an HTML file containing all generated songs.
11. Open the downloaded HTML file and click **Play** on any card.

## Playback and Compatibility

The **Play** button plays the selected card and stops the other cards. Audio is not muted automatically. If the browser cannot play a specific MP4, the grid keeps the button in the **Play** state and displays an error message.

Chrome or Edge is recommended. If the browser restricts local resources when opening files directly, serve the project folder through a local HTTP server.

## Troubleshooting

- **Covers are not visible:** make sure the HTML file was downloaded completely and that the browser can load the embedded image or video data.
- **All videos show the same image:** remove any shared `poster="imagen.png"` from an old grid. The current generator assigns an individual cover to each song.
- **Play does not start:** confirm that the MP4 is valid and try an up-to-date version of Chrome or Edge.
- **Generation fails:** check the Pollinations AI API key, its permissions or balance, and the network connection.
- **Lyrics are missing:** check that the API key can access the text model used for lyrics generation. The generated lyrics are then sent to Lyria as part of the music prompt.

## Credits

Designed by **Juan Guillermo Rivera Berrio** with Gemini 3 and Antigravity assistance.

This project is part of a series of creative tools developed for AI-assisted artistic exploration in 2026.
