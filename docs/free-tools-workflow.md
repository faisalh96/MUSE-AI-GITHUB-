# Free tools workflow

This project uses free tools to turn Muse AI artwork into 28-second Bengali cartoon reels.

## Tools

| Purpose | Free tool |
|---|---|
| 3D scenes, posing, camera animation, rendering | [Blender](https://www.blender.org/) |
| Video editing and captions | [Kdenlive](https://kdenlive.org/) |
| Bengali narration recording and cleanup | [Audacity](https://www.audacityteam.org/) |
| Image preparation | [Krita](https://krita.org/) or [GIMP](https://www.gimp.org/) |
| Video conversion and compression | [FFmpeg](https://ffmpeg.org/) |
| Bengali font | [Noto Sans Bengali](https://fonts.google.com/noto/specimen/Noto+Sans+Bengali) |

## 28-second reel setup

- Output resolution: `1080 × 1920`
- Aspect ratio: `9:16`
- Frame rate: `30 fps`
- Total frames: `840`
- Audio format: `48 kHz WAV`
- Video format: `MP4/H.264`

## Production stages

### 1. Design in Muse AI

1. Create an original character sheet.
2. Create matching side, front, and action poses.
3. Create backgrounds for all reel scenes.
4. Export high-resolution PNG reference artwork.
5. Avoid generating copyrighted characters or copying watermarks and logos.

### 2. Prepare artwork

1. Open files in Krita or GIMP.
2. Add transparent backgrounds when required.
3. Separate foreground, character, and background layers.
4. Export prepared PNG files.

### 3. Build the scene in Blender

1. Configure the output to 1080 × 1920.
2. Set frame rate to 30 fps.
3. Set the scene length to 840 frames.
4. Add the prepared pictures as textured planes or 3D cards.
5. Add a 9:16 camera.
6. Create slow, keyframed camera and character moves.
7. Add soft lighting and keep the style consistent.

For a simple first reel, use 2.5D movement: static artwork plus keyframed zoom, pan, and character or prop motion.

### 4. Record narration

1. Write the Bengali script.
2. Record each sentence in Audacity.
3. Remove noise and normalize the volume.
4. Export a 48 kHz WAV file.
5. Leave time for the opening and closing cards.

### 5. Edit in Kdenlive

1. Import rendered video and narration.
2. Align scenes with spoken words.
3. Add Noto Sans Bengali subtitles or captions.
4. Add gentle licensed music at low volume.
5. Add an original channel card or remove all third-party branding.
6. Export an H.264 MP4.

### 6. Compress with FFmpeg

Example command:

```bash
ffmpeg -i final.mov -c:v libx264 -pix_fmt yuv420p -c:a aac -b:a 192k final.mp4
```

Adjust the input filename only; keep the output resolution and 9:16 frame shape unchanged.

## Recommended folder placement

- Muse AI exports: `assets/`
- Edited transparent PNGs: `assets/characters/` or `assets/environments/`
- Blender scenes: `blender/scenes/`
- Blender scripts: `blender/scripts/`
- Preview renders: `blender/renders/`
- Final video: `exports/video/`
- Narration: `exports/audio/`
