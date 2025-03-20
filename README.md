✨ NLogger - Minecraft Chat Logging & Discord Integration Plugin
Overview
NLogger is a Minecraft plugin designed for chat logging, command monitoring, and Discord integration. It allows server administrators to monitor in-game chat messages, track player commands, and store death messages in a dedicated Discord channel in real time.

---------------------------------------------------------------

Features
✅ Chat Logging – Captures all in-game chat messages and logs them to a Discord channel.
✅ Command Logging – Tracks and logs all player commands executed on the server.
✅ Death Message Logging – Sends player death messages to a specified Discord channel.
✅ Discord Integration – Uses JDA (Java Discord API) to send chat messages to a designated Discord text channel.
✅ Chat Formatting – Supports color codes.
✅ Configurable Settings – Enable or disable logging, choose between plain text or embedded messages, customize the Discord channel, and select embed message colors.
⚡ Optimized Performance – Uses efficient asynchronous processing to prevent lag.

---------------------------------------------------------------

How It Works?
⚡Player Sends a Message or Executes a Command – The plugin captures the action immediately.
⚡Message Formatting – The plugin removes color codes (if necessary) before sending it to Discord.
⚡Discord Logging – The formatted message is sent to the specified Discord channel as either plain text or an embedded message
---------------------------------------------------------------

Example Output Chat
️ On Discord (if Embed mode is enabled):


---------------------------------------------------------------


Conclusion
NLogger is a powerful and easy-to-use plugin for Minecraft servers that want to log chat activity, monitor player commands, and track player deaths.
It is perfect for server moderators, community managers, and chat administrators.

---

## ⚙ Configuration
The plugin uses a `config.yml` file where you can customize the following:

```yaml
language: "en.yml" # Options: "en.yml" or "cz.yml"
mysql:
  enabled: false
  host: "localhost"
  port: 3306
  database: "minecraft"
  user: "root"
  password: "password"

discord:
  token: "YOUR_DISCORD_BOT_TOKEN_HERE"  # ⚠️ Nastavte správný token!

DeathMessage:
  Enabled: false  # Pokud je false, zprávy se nebudou posílat
  Channel_deadmessage: "123456789012345678"  # Discord ID kanálu (NE název kanálu!)

ChatLog:
  Enabled: false
  Channel: "1170059765825667162" # ID kanálu na Discordu
  Embed: true         # Pokud je true, zprávy budou v embedu
  Color: "#3498db"    # Barva embedu (např. modrá)

CommandLog:
    Enabled: false
    Channel: "1242095233982922752" # ID Discord kanálu
    Embed: true
