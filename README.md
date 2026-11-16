# Video Claw PR evidence

Public screenshots and interaction GIF recordings used in Video Claw pull request descriptions. This repository contains project review evidence, not user uploads or production media.

## Use an image

```markdown
![Description](https://cdn.jsdelivr.net/gh/BANG404/video-claw-pr-evidence@FULL_COMMIT_SHA/video-claw/pr-NUMBER/screenshot.png)
```

Pin the complete Git commit SHA. To update a screenshot, commit the new image and use the new commit SHA in the PR description. Do not use a moving branch URL.

Only publish screenshots reviewed for public disclosure. Keep credentials, personal data, user assets and production media out of this repository. Original product and third-party marks retain their respective rights.

`manifest.json` records each screenshot's source commit, source path, related PR and SHA-256 checksum. Static screenshot bytes match the existing review screenshots. GIF entries additionally record capture conditions and simulation boundaries.

## Update procedure

1. Copy reviewed screenshots into `video-claw/pr-NUMBER/`.
2. Update `manifest.json` with source attribution and SHA-256 checksums.
3. Commit and push to `main`.
4. Build jsDelivr links using the complete new commit SHA.
5. Verify HTTP 200, image content type and matching SHA-256 before changing PR descriptions.
6. Replace only image links, preserving the PR's technical description and validation results. Read the saved PR description again to verify the result.

## Interaction GIFs

Use a real browser recording for loading, success, failure, retry and other state changes. Preserve elapsed frame times and the readable result states; merge identical consecutive frames when encoding. Prefer short loops and keep the text legible. Use the same commit-pinned Markdown links as PNGs, with a `.gif` filename, and make each preview clickable to its GitHub original.

The PR #1045 recording exercises the real Vue diagnostics component against an isolated desktop bridge fixture. It demonstrates UI behavior, not a live log upload. The fixture returns after 1200 ms to make the loading state visible. Browser interaction assertions cover the receipt, cleared success after failure, and successful retry. Its 94 captured frames encode to eight changed frames while preserving the recorded duration.

Verify GIF signature/content type, checksum, frame count, loop duration and actual browser playback. Test jsDelivr using normal browser requests too: a successful download with identity encoding alone does not establish successful embedding. Record CDN errors and PR page login limitations accurately.
