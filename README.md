# Trip Fieldnotes

**English** | [简体中文](README.zh-CN.md)

The trip side of [Fieldnotes](https://github.com/Tangerineeew/fieldnotes) for [TREK](https://github.com/mauriceboe/TREK). It adds a **Trip Fieldnotes** tab to every trip, where the whole group reads the notes that have been shared with that trip, organises them into trip folders, and turns the useful parts into the day plan.

## What it does

- **Everything shared with the trip, in one place.** Live references always show the latest version of the original note. Snapshots show the version that was frozen when it was added, with their own copies of the images, and stay readable even after the original is deleted or its author leaves the trip.
- **Trip folders.** Group the trip's notes into folders such as "Arrival" or "Day 1", independently of how each author files the original in their own library.
- **Start notes from the trip.** "New note for this trip" opens the Fieldnotes editor and, when you save, keeps a private original in your library and links it to the trip in one step.
- **Into the day plan.** Copy an excerpt of up to 500 characters from any note into a day of the trip as a regular TREK day note. The original is never changed.
- **Respects trip roles.** Everyone on the trip can read; only people who may edit the trip can add, remove or reorganise notes.
- **Fourteen languages,** following TREK's language setting, including right-to-left layout for Arabic.

## Screenshots

![A live reference opened in a trip's Fieldnotes tab](./docs/screenshot.png)

## Permissions

Trip Fieldnotes requests no permissions of its own: its manifest lists none. Everything it shows or changes goes through the `trip` function exported by the Fieldnotes plugin, which TREK runs as the signed-in user. It can therefore only read the trips you belong to and only change the ones you may edit, and the permissions Fieldnotes itself needs are explained in [its README](https://github.com/Tangerineeew/fieldnotes#permissions).

## Setup

1. Install and enable [Fieldnotes](https://github.com/Tangerineeew/fieldnotes) first. Trip Fieldnotes declares it as a dependency and cannot run without it.
2. In TREK, open **Admin → Plugins**, install **Trip Fieldnotes**, and enable it. Uploaded plugins start disabled.
3. Open any trip and choose the **Trip Fieldnotes** tab. Share notes from the Fieldnotes library with "Bring into a trip", or create one here with "New note for this trip".

Uninstalling Trip Fieldnotes only removes the tab. The notes, trip links and snapshots belong to Fieldnotes and stay there.

## Source

This repository holds the built plugin. Its small server entry point is `server/index.js`; the interface is the same client that Fieldnotes ships, and both are built from the [`source/`](https://github.com/Tangerineeew/fieldnotes/tree/main/source) directory of the Fieldnotes repository.

## License

[MIT](./LICENSE)
