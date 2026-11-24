# ssg-videos-temp

Public media host for the ssg-videos clients.

## Releases (current)

Every approved video and its cover is published as a **GitHub Release**, one per video:

- Tag: `<client>/<slug>` (for example `signature-smile/caries`)
- Assets: `<slug>.mp4` (the approved video) and `<slug>.jpg` (its cover)
- URL: `https://github.com/imenesesl/ssg-videos-temp/releases/download/<client>/<slug>/<slug>.mp4`

These URLs are permanent. Buffer reads the video from them, and the client portal shows and
downloads them. They are published by `scripts/publish-media.mjs` in the main ssg-videos repo,
which also records them in `clients/<client>/media.json`. Release assets do not count toward the
git repo's size.

## `upload/<slug>` branches (legacy)

Before Releases, each video was pushed to its own `upload/<slug>` branch and Buffer read it from
raw.githubusercontent.com. Those branches stay as they are until their posts are published; no
new ones are created. `main` holds only this README.
