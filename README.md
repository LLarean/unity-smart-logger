# ![unity](https://img.shields.io/badge/Unity-100000?style=for-the-badge&logo=unity&logoColor=white) SmartLogger

[![Releases](https://img.shields.io/github/v/release/llarean/unity-smart-logger)](https://github.com/llarean/unity-smart-logger/releases)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/LLarean/unity-smart-logger/blob/master/LICENSE.txt)
![stability-stable](https://img.shields.io/badge/stability-unstable-yellow.svg)
[![Tests](https://img.shields.io/badge/Tests-NUnit-green.svg)]()
[![CodeFactor](https://www.codefactor.io/repository/github/llarean/unity-smart-logger/badge)](https://www.codefactor.io/repository/github/llarean/unity-smart-logger)
[![Status](https://img.shields.io/badge/Development-Paused-orange)](https://GitHub.com/llarean/unity-smart-logger/graphs/commit-activity)

> **Work in progress** — not production-ready.

Extends Unity's `Debug.Log` with automatic caller information, color-coded output, configurable log levels, and zero overhead in production builds.

## Quick Start

Install via Package Manager: `https://github.com/llarean/unity-smart-logger.git`

Or clone and add as a local package via **Window → Package Manager → Add package from disk**.

```csharp
using SmartLogger;

SmartLogger.Log("Player spawned");
SmartLogger.Log("Low health", LogLevel.Important);
SmartLogger.LogWarning("Save file missing");
SmartLogger.LogError("Physics engine failed");
SmartLogger.LogException(ex, "Collision error");
SmartLogger.LogIf(frameTime > 16.67f, $"Frame drop: {frameTime:F2}ms");
```

Console output:

```
[12.34s] [PlayerController.Start:15] 'Player spawned'
[12.35s] [GameManager.LoadLevel:42] 'Loading level: Forest'
```

## Configuration

Create a config asset via **Assets → Create → SmartLogger → Config**, or open **Tools → Smart Logger → Settings**.

| Setting | Description | Default |
|---------|-------------|---------|
| Log Display Level | Minimum importance level to display | Verbose |
| Enable In Build | Enable logging in production builds | false |
| Show Timestamp | Show elapsed time since session start | true |
| Enable Color Coding | Color-coded output by log type | true |
| Max Cache Size | Maximum cached caller info entries | 1000 |

The settings window also shows cache statistics and allows manual cache clearing.

## Roadmap

- [ ] Remote logging — send logs to external services
- [ ] Log categories — filter by custom tags
- [ ] File output — persist logs between sessions
- [ ] Visual log viewer — in-editor log browser
- [ ] Performance profiler — built-in frame metrics

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## License

MIT — see [LICENSE.md](LICENSE.md).

---

<div align="center">

**Made with ❤️ for the Unity community**

[⭐ Star on GitHub](https://github.com/llarean/unity-smart-logger) • [📚 Documentation](Documentation~/index.md) • [🐛 Issues](https://github.com/llarean/unity-smart-logger/issues)

</div>
