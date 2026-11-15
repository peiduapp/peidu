# Pindu website

The public website for Pindu, the iPhone app that reads Chinese text through the camera and shows
pinyin above and English below. Served by GitHub Pages at https://pinduapp.github.io/pindu/.

Plain HTML and CSS, no build step. Edit a file, merge to `main`, and GitHub Pages publishes it
within a minute or two.

## Files

| File | What it is |
| :--- | :--- |
| `index.html` | Home page: hero, feature blocks, privacy, Premium |
| `support.html` | Help page. App Store Connect links to this path, so it must not move |
| `privacy.html` | Privacy policy. App Store Connect links to this path, so it must not move |
| `about.html` | Why Pindu exists, how it works on-device, credits |
| `assets/site.css` | Shared styles, including light and dark mode |
| `assets/img/` | Screenshots, app icon, and Apple's App Store badge |
| `CLAUDE.md` | Rules for anyone (or any AI assistant) editing this repo |

## Common changes

**Switch the home page from "coming soon" to the App Store badge.** Open `index.html` and find
the comment that starts `HERO BUTTON`. Delete the block marked `cta-prelaunch`, remove the
`<!--` and `-->` lines around the block marked `cta-launch`, and replace `APP_STORE_URL` with the
app's App Store link.

**Change the Premium price.** Nothing to do here: the site shows no price on purpose. Change it in
App Store Connect.

**Add or replace a screenshot.** Originals live in the app repo under `marketing/`. Shrink to
720 pixels wide, save as WebP, and put the file in `assets/img/`. On the home page each phone is cropped
below its content: set `--crop: 720 / H` on its `phone` div, where H is the screenshot's height in
pixels down to about 110 pixels below the last thing worth showing.

## Contact

hellopindu@gmail.com
