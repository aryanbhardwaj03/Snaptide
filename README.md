# Any Video Download

A local web app for downloading public or permissioned videos from supported social platforms using `yt-dlp`.

This app intentionally does not bypass private accounts, DRM, paywalls, platform access controls, or authorization checks. Use it only for media you own, public media, or content you have permission to download.

By default, video downloads use the best available quality up to 1080p. Paste a valid URL and the 1080p download option is enabled immediately while metadata and higher-quality choices load in the background. Downloads run as background jobs with progress polling, so the page stays responsive.

## Run

```powershell
python server.py
```

Open:

```text
http://localhost:3000
```

## Required Tools

Install `yt-dlp` and make sure it is available in your PATH:

```powershell
winget install yt-dlp.yt-dlp
```

Optional but recommended for merging high-quality video and audio:

```powershell
winget install Gyan.FFmpeg
```

## Supported Platforms

The app accepts URLs from YouTube, X/Twitter, Instagram, Facebook, LinkedIn, Bluesky/Bsky, Dailymotion, Reddit, and other hosts supported by `yt-dlp` when they are publicly accessible or otherwise legally accessible to you.

Downloaded files are stored in the local `downloads` folder and the browser automatically starts saving the completed file to your device.

## Optional Node Backend

`server.js` and `package.json` are included if you prefer a Node/Express backend on a machine with Node.js installed:

```powershell
npm install
npm start
```
