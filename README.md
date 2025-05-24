# 🛡️ PluginHiderX

<div align="center"> 

<div align="center">
  <img src="https://raw.githubusercontent.com/teaminfinitydev/teaminfinitydev/refs/heads/main/img/pluginhiderx-banner.svg" alt="AntiDDoSPro Banner">
</div>

[![Paper 1.21.1](https://img.shields.io/badge/Paper-1.21.1-orange.svg)](https://papermc.io/)
[![Release](https://img.shields.io/github/v/release/teaminfinitydev/PluginHiderX?include_prereleases&style=flat-square)](https://github.com/teaminfinitydev/PluginHiderX/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/teaminfinitydev/PluginHiderX/total?style=flat-square)](https://github.com/teaminfinitydev/PluginHiderX/releases)
[![Contributors](https://img.shields.io/github/contributors/teaminfinitydev/PluginHiderX?style=flat-square)](https://github.com/teaminfinitydev/PluginHiderX/graphs/contributors)
[![License](https://img.shields.io/github/license/teaminfinitydev/PluginHiderX?style=flat-square)](LICENSE)

*A powerful Minecraft plugin that protects your server by hiding plugins from unauthorized players*

[Installation](#-installation) • 
[Commands](#-commands) • 
[Permissions](#-permissions) • 
[Configuration](#-configuration) • 
[Support](#-support)

</div>

## ✨ Features

- **Comprehensive Protection**: Blocks all plugin list commands (`/plugins`, `/pl`, etc.)
- **Version Command Protection**: Optionally hides version information (`/version`, `/ver`, etc.)
- **Permission System**: Granular control over who can view plugin information
- **Customizable Messages**: Change all messages in the config
- **Lightweight**: Minimal performance impact on your server
- **Auto-Update Checker**: Notifications when new versions are available
- **Tab Completion**: Easy-to-use command tab completion

## 📥 Installation

### Requirements
- Paper 1.21.1 or higher
- Java 21 or higher

### Steps
1. Download the latest version from the [Releases](https://github.com/teaminfinitydev/PluginHiderX/releases) page
2. Place the JAR file in your server's `plugins` folder
3. Restart your server
4. Enjoy the protection!

## 🔧 Commands

| Command | Description |
|---------|-------------|
| `/pluginhiderx` or `/phx` | Show plugin information |
| `/pluginhiderx reload` | Reload the plugin configuration |
| `/pluginhiderx info` | Display detailed plugin information |
| `/pluginhiderx test` | Test your permissions |
| `/pluginhiderx debug` | Show debug information (admin only) |

## 🔑 Permissions

| Permission | Description | Default |
|------------|-------------|---------|
| `pluginhiderx.viewplugins` | Allows seeing server plugins | `false` |
| `pluginhiderx.bypass` | Bypasses all plugin hiding restrictions | `false` |
| `pluginhiderx.admin` | Access to admin commands | `op` |

## ⚙️ Configuration

The default `config.yml` file:

```yaml
settings:
  debug: false
  block-version-commands: true
  additional-blocked-commands:
  - about
  - icanhasbukkit

messages:
  no-permission: "&cYou don't have permission to view server plugins!"
  unknown-command: "&cUnknown command. Type \"/help\" for help."
  prefix: "&7[&6PluginHiderX&7]&r "

advanced:
  send-fake-unknown-command: false
  log-blocked-attempts: true
  log-message: "Player {player} tried to use blocked command: {command}"
```

### Configuration Explanation

#### Settings
- `debug`: Enable debug mode
- `block-version-commands`: Block `/version` and similar commands
- `additional-blocked-commands`: Add more commands to block

#### Messages
- `no-permission`: Message sent when a player lacks permission
- `unknown-command`: Message sent when using fake unknown command
- `prefix`: Plugin message prefix

#### Advanced
- `send-fake-unknown-command`: Send unknown command message instead of permission error
- `log-blocked-attempts`: Log when players attempt to view plugins
- `log-message`: Format of the log message


## 🔄 Updates

PluginHiderX automatically checks for updates on startup. When a new version is available, a notification will appear in the console and in-game for administrators.

## 📊 Metrics

PluginHiderX collects anonymous usage statistics to help improve the plugin. You can opt-out by setting `metrics.enabled` to `false` in the config.

## 👥 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please make sure to test your changes before submitting a pull request.

## 📝 License

PluginHiderX is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🌐 Support

Need help with PluginHiderX?

- [GitHub Issues](https://github.com/teaminfinitydev/PluginHiderX/issues)
- [Website Support](https://codenexa.online/developers)

---

<div align="center">

Made with ❤️ by [Chamika Samaraweera](https://github.com/teaminfinitydev)

[![Web](https://img.shields.io/badge/Web-TeamInfinity-blue)](teaminfinity.pro)
[![Twitter Follow](https://img.shields.io/twitter/follow/teaminfdev?style=social)](https://twitter.com/teaminfdev)

</div>
