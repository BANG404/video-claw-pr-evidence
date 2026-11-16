# Video Claw PR evidence

Public screenshots used in Video Claw pull request descriptions. This repository contains project review evidence, not user uploads or production media.

## Use an image

```markdown
![Description](https://cdn.jsdelivr.net/gh/BANG404/video-claw-pr-evidence@FULL_COMMIT_SHA/video-claw/pr-NUMBER/screenshot.png)
```

Pin the complete Git commit SHA. To update a screenshot, commit the new image and use the new commit SHA in the PR description. Do not use a moving branch URL.

Only publish screenshots reviewed for public disclosure. Keep credentials, personal data, user assets and production media out of this repository. Original product and third-party marks retain their respective rights.

`manifest.json` records each screenshot's source commit, source path, related PR and SHA-256 checksum. The image bytes match the existing review screenshots.

## Update procedure

1. Copy reviewed screenshots into `video-claw/pr-NUMBER/`.
2. Update `manifest.json` with source attribution and SHA-256 checksums.
3. Commit and push to `main`.
4. Build jsDelivr links using the complete new commit SHA.
5. Verify HTTP 200, image content type and matching SHA-256 before changing PR descriptions.
6. Replace only image links, preserving the PR's technical description and validation results. Read the saved PR description again to verify the result.
