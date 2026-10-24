# Orbit v0.2.0 preview

[Download Windows x64](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-win-x64.exe) · [All platform downloads](https://github.com/luckypolamreddy/orbit-downloads#readme) · [SHA256SUMS.txt](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/SHA256SUMS.txt)

This release provides desktop development installers for Windows x64/ARM64, macOS Intel/Apple silicon and Linux x64/ARM64. It is a **preview for controlled testing**. Installers are unsigned; macOS builds are not notarized. Security review and testing coverage across real operating systems, devices, native control and networks remain pending.

## Available behavior

- Code-based rooms with admission, owner-selected screen sharing and separately approved desktop control. Sharing status and Stop controls remain visible.
- A fixed one-hour room lifetime. Expiry stops capture/control; continuing requires a fresh room and code.
- Private typed messages and optional browser-dependent microphone dictation. Manual Presentation mode hides private text and drafts on the user's own Orbit screen before an entire-display share in Teams.
- No recent-meeting history. Local profile, settings and planned schedules remain on the device.

## Setup and limitations

The installed desktop app includes its runtime; end users do not need Node.js or npm. **The Orbit backend is not bundled.** Participants must configure a shared Orbit server URL in Settings. The current localhost service on port 8787 works only on the same computer. Cross-laptop use requires a reachable `wss://` server and appropriate network setup; a shared public server has not yet been deployed.

macOS capture and control depend on screen-recording and Accessibility permissions. Linux native control requires X11 and a working optional driver. Missing native dependencies or permissions can disable control. Browser and platform differences require hands-on testing; producing an installer does not validate capture/control on that OS.

Dictation depends on browser speech recognition and may be unavailable in the desktop app. Microphone audio may be processed by the browser's speech provider. Typed messages remain available. Presentation mode must be enabled manually before external screen sharing and hides text on the local screen too.

Follow the [controlled testing checklist](https://github.com/luckypolamreddy/orbit-downloads/blob/main/TESTING.md) when evaluating this preview.
