# Orbit v0.2.0 preview downloads

**[Download Orbit for Windows Intel/AMD (x64)](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-win-x64.exe)**

| System | Installer |
| --- | --- |
| Windows Intel/AMD | [Windows x64 setup](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-win-x64.exe) |
| Windows ARM | [Windows ARM64 setup](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-win-arm64.exe) |
| macOS Intel | [Intel DMG](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-mac-x64.dmg) |
| macOS Apple silicon | [Apple silicon DMG](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-mac-arm64.dmg) |
| Linux Intel/AMD | [x64 AppImage](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-linux-x86_64.AppImage) · [amd64 DEB](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-linux-amd64.deb) |
| Linux ARM | [ARM64 AppImage](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-linux-arm64.AppImage) · [ARM64 DEB](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/Orbit-0.2.0-linux-arm64.deb) |

[Download SHA256SUMS.txt](https://github.com/luckypolamreddy/orbit-downloads/releases/download/v0.2.0/SHA256SUMS.txt) to check the installer against its published SHA-256 checksum. Checksums verify file integrity; these development installers are unsigned and macOS builds are not notarized. Platform trust checks may warn or block installation.

This is a **preview development build for controlled testing**. Security review and coverage across real devices, operating systems and networks remain pending. This repository distributes installer binaries and download documentation.

## Install and connect

Run the Windows setup wizard, open the macOS DMG and drag Orbit to Applications, or use your Linux package installer for the DEB. For an AppImage, allow execution in its file properties and open it. Node.js and npm are not needed to use the installed app.

**The backend is not bundled.** In Orbit's **Settings**, every participant needs the same shared Orbit server URL. Connections between laptops require a reachable `wss://` server and suitable network configuration. A shared public server has not yet been deployed. The current local service at `ws://127.0.0.1:8787/ws` supports clients on the same computer only; these downloads do not provide cross-laptop meetings out of the box.

Once a suitable server is available, create a room, share its 12-digit code and admit the joining participant. Admission codes expire after 15 minutes; the host can issue a fresh invitation without extending the room deadline. Microphone and camera start off. The owner selects what to share and separately approves desktop control; sharing and Stop controls remain visible. Control requires sharing the primary entire monitor; window sharing is view-only. Each control approval lasts up to 10 minutes. macOS requires screen-recording and Accessibility permissions for the relevant features. Linux desktop control requires X11 and a working optional native driver; unavailable drivers or permissions can leave control disabled.

Rooms have a fixed one-hour deadline from creation. Expiry stops capture and control. Continue in a fresh room with a new code. Orbit keeps no recent-meeting history; local profile, settings and planned schedules remain on the device.

Private messages support typing. Optional microphone dictation depends on browser and speech-service support and may be unavailable in the desktop app. Recognition may send microphone audio to the browser's speech provider. Manually enable **Presentation mode before sharing your entire display in Teams**: it hides private text and drafts on your own Orbit screen too. It does not automatically detect an external screen share.

Use the download links on this page. This preview's in-app download dialog still points to older private build artifacts; it will be updated in a later build.

See [testing steps](TESTING.md) and [release notes](RELEASE_NOTES.md).
