# SpotiGo

An Android app that lets you control and play Spotify through a custom native player shell, using a JavaScript event bridge to connect native Android controls with the web player.

💬 **Join the community:** https://discord.com/invite/ADHdD3MGgX — talk to me directly, request features, or report bugs.

## Overview

SpotiGo hosts the Spotify Web Player and layers native Android functionality on top of it — media controls, notifications, background playback, and more — via an embedded extension injected into the page. Communication between the native Kotlin layer and the web player happens through a custom bridge script that spans multiple JavaScript execution contexts.

**This is not a WebView-based solution.** SpotiGo __does not__ rely on installing a custom certificate to intercept and modify outgoing traffic. Doing so would require the user to trust a root certificate capable of man-in-the-middling their own traffic, which is a **dangerous practice** and something this project explicitly avoids. Instead, SpotiGo uses a custom engine, allowing script injection and event bridging without touching or decrypting network traffic at all.

## Features

- Runs the Spotify Web Player in a native Android shell
- Background playback
- Native media session integration (lock screen controls, notifications, etc.)
- Partial Android Auto support
- Bidirectional event bridge between the web player and native Android code
- No certificate installation, no traffic interception, no MITM

## Project Status

This project is unfinished and under active development. **Source code is not published** at this stage, both to avoid premature clones of incomplete software and to reduce the chance of the underlying method being noticed and patched before the project is ready. This repository serves as a public-facing overview of the project rather than a source distribution.

## License

No license has been assigned. All rights reserved.

## Contributing

Not currently accepting external contributions since the source isn't public. Feel free to open an issue for bugs or suggestions once builds are available.
