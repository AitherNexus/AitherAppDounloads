# Aither App Downloads

Central download hub for official Aither desktop applications.

## Distribution model

- **Source code:** Aither repositories
- **Windows installers:** GitHub Releases
- **Builds:** created outside GitLab CI, so publishing releases does not consume AitherNexus GitLab pipeline minutes
- **This repository:** download website + release/distribution documentation

## Release naming

Use one GitHub Release per Aither desktop release:

`Aither Apps vX.Y.Z`

Attach the finished installers directly to that release.

### Windows assets

Recommended filenames:

- `AitherApps-Setup-X.Y.Z.exe` — normal Windows installer
- `AitherApps-Portable-X.Y.Z.exe` — optional portable build

### Future platforms

- `AitherApps-X.Y.Z.dmg` — macOS
- `AitherApps-X.Y.Z.AppImage` — Linux

## Planned repository layout

```
AitherAppDounloads/
├── .github/
├── releases/
│   ├── windows/
│   ├── macos/
│   └── linux/
├── index.html
└── README.md
```

The `releases/` directories are documentation/placeholders only. **Do not commit large binary installers to the Git repository.** Put the actual `.exe`, `.dmg`, and `.AppImage` files on GitHub Releases.

## Current Aither Apps

The desktop hub can provide access to:

- Aither Weather
- Aither Clock
- Aither Notes
- Aither Maps
- Aither Calculator
- Aither Dashboard
- Aither Files
- Aither Mail
- Aither Gaming
- Aither AI
- Aither Web

## Publishing a Windows release

1. Build the Windows `.exe` outside GitLab CI.
2. Open the **Releases** page for this repository.
3. Create a new tag such as `v1.0.0`.
4. Name the release **Aither Apps v1.0.0**.
5. Upload `AitherApps-Setup-1.0.0.exe`.
6. Optionally upload the portable build.
7. Publish the release.
8. The Aither App Downloads website can link to the latest release.

## Important

GitHub Releases **stores and distributes** the finished installers; it does not magically compile an `.exe`. The executable must be built first.

Repository owner: **AitherNexus**
