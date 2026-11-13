# DOTTY VIEWER

A black-and-purple Second Life viewer community build based on Aurora Viewer.

## Current implementation

The DOTTY branch now applies its identity to the viewer itself:

- Custom DOTTY splash-screen and in-app logo asset.
- Custom DOTTY Windows application icon.
- Windows executable product name, description, and original filename.
- Window title shown as DOTTY VIEWER plus the viewer version.
- Default dark black/violet interface theme.
- Windows x64 GitHub Actions build and ZIP artifact workflow.

The Rust package name remains `aurora-viewer` internally because this branch builds the existing Aurora workspace. The distributed executable is named `DottyViewer.exe`.

## Build status

A Windows runner has now passed job setup and source checkout after the repository was renamed. The current Windows build is running; do not treat an artifact as available until the Actions run reports success and lists the `DOTTY-Viewer-Windows-x64` artifact.

A successful compile does not replace runtime validation. This build has not yet been tested through a full Second Life login/live-grid session. It is unsigned.

## Build it

1. Open the repository's **Actions** tab.
2. Select **DOTTY Viewer Windows Build**.
3. Select **Run workflow** on branch `dotty-viewer/windows-build`.
4. When the run completes successfully, download `DOTTY-Viewer-Windows-x64`.
5. Extract the ZIP and run `Start-DOTTY-Viewer.cmd`.

The artifact is temporary (14-day retention).

## Requirements

Windows 10/11 x64, a Vulkan-capable GPU/driver, and the Microsoft C++ build tools for local builds. The viewer connects to Second Life only when you log in with your own account. Never put account passwords in build files, scripts, or GitHub Actions.

## Upstream and license

Based on Aurora Viewer, GPL-3.0-or-later. Preserve LICENSE, NOTICE, and upstream attribution. DOTTY VIEWER is an independent community build and is not endorsed by Linden Lab or the Aurora Viewer team.
