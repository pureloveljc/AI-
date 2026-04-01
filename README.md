# youtube-interview-shorts-zh

Codex skill for turning a long YouTube interview, talk, or podcast into 5 to 8 short clips with Chinese hard subtitles.

## What It Does

- Downloads the source video and available subtitles from YouTube
- Parses the subtitle track into JSON for transcript analysis
- Helps select strong standalone moments for short-form distribution
- Cuts sub-3-minute clips
- Windows local subtitles for each clip
- Burns Chinese subtitles and a first-second title into each exported video

## Skill Trigger

Mention:

```text
$youtube-interview-shorts-zh
```

Example:

```text
Use $youtube-interview-shorts-zh to turn this YouTube interview URL into 5 to 8 Chinese-subbed short clips.
```

## Repository Layout

```text
.
├── SKILL.md
├── agents/openai.yaml
├── scripts/
├── references/
```

## Install Into Codex

Copy this repository folder into:

```text
~/.codex/skills/youtube-interview-shorts-zh
```

Or install it with your preferred Codex skill import flow from GitHub.

## Runtime Notes

- `yt-dlp` must be available in the environment
- `ffmpeg` must be available, or the bundled scripts will try the `imageio-ffmpeg` fallback
- The downloader prefers Chrome cookies and may need refreshed browser login state if YouTube blocks downloads
- When English subtitles are unavailable, the workflow can fall back to `zh-Hans`

## License

MIT
