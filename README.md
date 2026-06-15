# FlashView

**Browse 100,000 photos. At the speed of thought.**

A fast, lightweight photo viewer for Windows — built for photographers who want to see and cull huge archives at speed.

> **Website & Download → [flashview.net](https://flashview.net)**
>
> This repo is the **issue tracker only**. Source code is not public (yet).

English · [Deutsch](README.de.md)

## What it does

Open a folder with thousands of photos. Scroll through them at full speed. Rate your keepers with a single keystroke, flag the rejects, filter down to what matters, and export ratings as standard XMP — ready for Lightroom, Bridge, Photo Mechanic, or digiKam.

FlashView is the fast first-pass tool between copying your card and opening your editor.

## What Sets It Apart

**Built for massive folders.** Virtualized grid, streaming thumbnails, no pre-indexing wait — stays responsive at 100,000+ images in a single folder.

**Browse at the speed of thought.** Cursor keys, mouse wheel, scroll — every input shows the next image with sub-50 ms latency, even on 45-megapixel JPEGs. That's the *Flash* in the name.

**Native Windows Explorer workflow.** Right-click any image → *Open with FlashView* → you're in Loupe in under a second, with the entire folder already loaded. `Ctrl+C` copies the image, arrow keys browse neighbors.

## Features

- **XMP metadata, shared with every major tool.** Ratings, color labels, and pick/reject flags are written as standard XMP — embedded inside the JPEG, or as a sidecar next to your RAW. Any XMP-aware program reads them back: Lightroom, Bridge, Photo Mechanic, digiKam, and anything else that speaks XMP.
- **Batch-rate hundreds at a time.** Select 200, 1,000, or more files — press `3`, done. Stars, color labels, pick/reject all writable in a single keystroke, across JPEGs and XMP sidecars alike. `Ctrl+Z` undoes the last batch.
- **Filter on the fly.** Filter by rating (at-least, exact, at-most), by color label, by picked, by rejected, or hide RAW files entirely. Cull down to exactly what you're reviewing.
- **Sort and group.** Name or date, ascending or descending. Group a parent folder by shoot, with configurable depth.
- **Five color labels.** Red (`6`), yellow (`7`), green (`8`), blue (`9`), purple (`V`) — written as standard XMP, read back everywhere.
- **Keyboard-first.** `←→` navigate, `0–5` rate, `P` pick, `X` reject, `U` clear flags, `G/L` Grid/Loupe, `F` fullscreen, `F11` second-monitor Loupe, `I` EXIF, `S` slideshow, `Ctrl+F` search, `Del` trash, `Ctrl+Z` undo, `Ctrl+A` select all, `Ctrl+O` open folder, `R` recursive, `F1` shows the full list.
- **Jump to any file.** Quick-open search (`Ctrl+F`) finds a folder or image by name across the whole tree.
- **Slideshow.** Auto-advance through the current folder or selection at a configurable interval (`S`).
- **Second-monitor Loupe.** `F11` opens a full-size Loupe on your second screen while you browse and cull on the main one.
- **Cloud-aware.** For OneDrive / Nextcloud / Dropbox folders, choose how online-only files are handled: fully sync (download all), ignore (no download), or preview just the first N images on demand — so a huge cloud folder opens without pulling everything down.
- **Drill up, drill down.** Open a parent folder and see shoots grouped. Zoom into any subfolder, or browse them all at once recursively.
- **Recent roots.** Your last opened folders, one click away.
- **Dark UI, DE/EN.** Follows your system language automatically.
- **Zoom and inspect.** 1:1 pixel view, fit-to-screen, pan.
- **EXIF panel.** Camera, lens, focal length, aperture, shutter, ISO, date, pixel size, artist, copyright — toggle in the Loupe with `I`.

## Supported formats

- **Images:** JPEG (`.jpg`, `.jpeg`, `.jpe`, `.jfif`), PNG, HEIC / HEIF (`.heic`, `.heif`, `.hif`), TIFF (`.tif`, `.tiff`)
- **RAW** — best-effort via embedded preview JPEG, no external RAW engine:
  - Canon CR3, CR2
  - Nikon NEF / NRW
  - Sony ARW / SR2
  - Fujifilm RAF
  - Adobe DNG (Leica M8 falls back to EXIF only)
  - Hasselblad 3FR / FFF
  - Samsung SRW
  - Pentax PEF
  - Olympus ORF (modern bodies; old compacts show only camera thumbnails)
  - Panasonic RW2

## What It's Not

- Not a developing tool — no exposure, crop, or white balance.
- Not color-managed yet — sRGB assumed.
- Not a library or catalog — folders are your catalog, no import step.

## Where it fits in

Most photo browsers promise speed. Most are fine at a few hundred images, fall behind at 10,000, and give up at 100,000. FlashView is built for the second half of that curve — the folders that real photographers actually accumulate.

Lightroom is editor-first; its Library isn't optimized for rapid culling. Photo Mechanic handles the scale but is priced for newsrooms. FlashView fills the gap: fast enough for a fifty-thousand-image shoot, lean enough to live on every machine you own.

## Ecosystem

FlashView works hand-in-hand with [StarRate](https://github.com/merlin1de/starrate) — a Nextcloud plugin for guest and model ratings. The full workflow: shoot → FlashView for your own first pass → upload to Nextcloud → StarRate collects external ratings → back in FlashView you see your own and the guest ratings consolidated, all in standard XMP.

## Feedback

Bug or feature idea? [Open an issue](../../issues/new). This repo is issue-only — no pull requests accepted, but bug reports, workflow critiques, and screenshots are very welcome.

## Background

Born out of my own Canon workflow (20D through R6 Mk III). Lightroom is excellent for developing, but the step *before* — clicking through 800 frames and marking the keepers — always felt sluggish. FlashView makes that step fast.

If you shoot similarly, it might be faster for you too.

---

© Mathias Mischler. Provided "as is", no warranty.
