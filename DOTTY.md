# DOTTY VIEWER

A Windows build track for a Second Life viewer based on Aurora Viewer.

## Build status

This branch adds a repeatable Windows x64 build workflow. It compiles the upstream
Rust viewer and packages it as `DottyViewer.exe` with a DOTTY launcher.

**Branding status:** the executable is currently the Aurora application binary
renamed for packaging and launched with the supported `--title` argument.
This does not yet replace every Aurora logo, splash screen, window title, or
in-app colour. Those changes require native integration in the Rust UI and
branding resources, followed by a successful Windows build and live-grid test.

## Build it

1. Open the repository's **Actions** tab.
2. Select **DOTTY Viewer Windows Build**.
3. Select **Run workflow** on branch `dotty-viewer/windows-build`.
4. Wait for the Windows job to complete.
5. Download the `DOTTY-Viewer-Windows-x64` artifact.
6. Extract the ZIP and run `Start-DOTTY-Viewer.cmd`.

The artifact is temporary (14-day retention). It is not code-signed.

## Requirements

Windows 10/11 x64 and a Vulkan-capable GPU/driver. The viewer connects to
Second Life only when you log in with your own account. Never put account
passwords in build files, scripts, or GitHub Actions.

## Upstream and license

Based on Aurora Viewer, GPL-3.0-or-later. Preserve LICENSE, NOTICE and
upstream attribution. This is an independent community build and is not
endorsed by Linden Lab or the Aurora Viewer team.
