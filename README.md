# Video Renderer

Cloud-based video rendering using GitHub Actions. Zero local compute needed!

## How it works

1. Push a job spec JSON to `jobs/` folder
2. Trigger the `render-video` workflow with the job ID
3. GitHub Actions renders the video using FFmpeg
4. Video is uploaded to catbox.moe
5. Result saved to `results/` folder

## Job Spec Format

Create a file like `jobs/my-video-123.json`:

```json
{
  "headline": "BREAKING NEWS",
  "slides": [
    {"image": "https://example.com/image1.jpg", "text": "Slide 1 headline"},
    {"image": "https://example.com/image2.jpg", "text": "Slide 2 text"},
    {"image": "https://example.com/image3.jpg", "text": "Slide 3 text"},
    {"image": "https://example.com/image4.jpg", "text": "Slide 4 text"},
    {"image": "https://example.com/image5.jpg", "text": "Final slide CTA"}
  ],
  "animation_style": "zoom_in",
  "music_url": null
}
```

## Animation Styles

- `zoom_in` - Ken Burns zoom in effect
- `zoom_out` - Ken Burns zoom out effect
- `pan_left` - Pan left to right
- `pan_right` - Pan right to left

## Output

Videos are 1080x1920 (9:16), 15 seconds, 30fps.
