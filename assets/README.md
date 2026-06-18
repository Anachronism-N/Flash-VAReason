# Assets

The project page renders the original figure PDFs directly to avoid blurry raster images.

Required figure files:

- `tease.pdf` — teaser / task definition figure
- `overview.pdf` — Flash-VAReason framework overview
- `case.pdf` — qualitative example figure

The demo is embedded from YouTube:

- https://youtu.be/7-h1yYGB0JI

Optional local video asset path, if a hosted MP4 is needed later:

- `demo_haiwei_v5.mp4`

Recommended encoding for GitHub Pages playback:

- H.264 video
- AAC audio
- `+faststart` MP4 metadata
- compressed web size when possible

Example ffmpeg command:

```bash
ffmpeg -i demo_haiwei_v5.mp4 \
  -vf "scale=-2:720" \
  -c:v libx264 -preset veryfast -crf 28 \
  -c:a aac -b:a 96k \
  -movflags +faststart \
  assets/demo_haiwei_v5.mp4
```
