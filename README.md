# hesbon-osoro.github.io

**Live site:** https://hesbon-osoro.github.io

This site mirrors the [hesbon-osoro profile README](https://github.com/hesbon-osoro/hesbon-osoro), so one file updates both the GitHub profile and the website.

## How it's built

- [`publish.yml`](.github/workflows/publish.yml) runs every 3 hours, and can also be started by hand.
- It checks out the profile repository and runs its [`scripts/site/build.mjs`](https://github.com/hesbon-osoro/hesbon-osoro/blob/main/scripts/site/build.mjs).
- That script renders `README.md` with GitHub's Markdown API, wraps it in a themed page, and copies in every image the README uses.
- Output only changes when the README or its stat cards change, and the workflow only commits when it does.

Everything in this repository except `.github/`, `README.md` and `.gitignore` is generated. Edit the profile README, not these files.

To publish immediately: **Actions → Publish from profile README → Run workflow**.
