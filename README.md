# Frusoft releases

Installers and downloads for Frusoft apps. Every app publishes its builds here as
[GitHub Releases](../../releases), so there is one place to find them and one URL pattern to link to.

## Apps

| App | What it is | Download |
| --- | --- | --- |
| Beatweave | DJ set planner for macOS that reads your Rekordbox library | [Beatweave 0.1.0 for macOS (Apple silicon)](https://github.com/frusoft/releases/releases/download/beatweave-v0.1.0/Beatweave_0.1.0_aarch64.dmg) |

## How releases are organised

- One release per app version, tagged `<app>-v<version>` (for example `beatweave-v0.1.0`).
- Installers are attached to the release as assets, named `<App>_<version>_<arch>.<ext>`.
- The latest build of an app is the release with the highest version for that app. Link to it with
  `https://github.com/frusoft/releases/releases?q=<app>` or to a fixed asset URL:
  `https://github.com/frusoft/releases/releases/download/<app>-v<version>/<file>`.

## Publishing a build

```bash
gh release create beatweave-v0.1.0 ./Beatweave_0.1.0_aarch64.dmg \
  --repo frusoft/releases --title "Beatweave 0.1.0" --notes "What changed."
```

Only signed (and, on macOS, notarised) installers are published here.
