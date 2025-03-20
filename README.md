# NLogger - Minecraft Chat Logging & Discord Integration Plugin

## 📖 Overview
**NLogger** is a Minecraft plugin designed for **chat logging and Discord integration**. It allows server administrators to **monitor in-game chat messages** and store them in a dedicated Discord channel in real time. Additionally, it supports **PlaceholderAPI** and **LuckPerms** for advanced chat formatting, including **prefixes, ranks, and placeholders**.

## ✨ Features
- 📝 **Chat Logging** – Captures all in-game chat messages and logs them to a Discord channel.
- 🤖 **Discord Integration** – Uses **JDA (Java Discord API)** to send chat messages to a specified Discord text channel.
- 🎨 **Chat Formatting** – Supports **color codes, PlaceholderAPI placeholders, and LuckPerms prefixes**.
- 🔄 **PlaceholderAPI Support** – Expands chat messages with dynamic placeholders like `%luckperms_prefix%` for player ranks.
- ⚙ **Configurable Settings** – Customize logging settings, choose between **plain text or Discord embed messages**, and define a **Discord channel for logs**.
- ⚡ **Optimized Performance** – Uses **asynchronous processing** to prevent lag.

---

## 🛠️ How It Works
1. **Player Sends a Message** – When a player types a message in the Minecraft chat, the plugin captures it.
2. **PlaceholderAPI Processing** – If **PlaceholderAPI** is installed, the message is expanded with placeholders like `%luckperms_prefix%`.
3. **Message Formatting** – The plugin formats the chat message, removes color codes (if needed), and prepares it for Discord.
4. **Discord Logging** – The formatted message is sent to a **specified Discord channel** as either **plain text** or an **embedded message**.

---

## 📦 Dependencies
To use **NLogger** effectively, ensure you have the following installed:

- 🏗 **Minecraft Server** (Spigot/Paper `1.21+`)
- ☕ **Java 17+**
- 📌 **PlaceholderAPI** *(Required for placeholders support)*
- 🏷 **LuckPerms** *(Optional, for rank prefixes)*
- 🖥 **JDA (Java Discord API)** *(For Discord integration)*

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
