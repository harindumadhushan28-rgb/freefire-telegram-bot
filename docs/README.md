# 🎮 Free Fire Telegram Bot

> [🇧🇷 Leia em Português](README.pt-br.md)

A Telegram bot built with **Spring Boot** that provides Free Fire player information and ban status checking using public APIs.

## ✨ Features

- `/ban <2138152569>` — Check if an account is banned (permanent or temporary)
- `/player <2138152569>` — View full player profile (nickname, level, rank, region, likes, guild, etc.)
- Input validation and error handling
- Clean architecture with separated services

## 🛠️ Tech Stack

- **Java 21**
- **Spring Boot 4**
- **Spring WebFlux** (WebClient for API calls)
- **TelegramBots 6.9.7.1**
- **Lombok**
- **Docker**

## 📡 APIs Used

| Feature | API |
|---------|-----|
| Player Info | `freefire-api-six.vercel.app` (0xMe/FreeFire-Api) |
| Ban Check | `ff.garena.com/api/antihack/check_banned` (Garena Official) |

## 🚀 Getting Started

### Prerequisites

- Java 21+
- Maven
- A Telegram Bot Token (get one from [@BotFather](https://t.me/BotFather))

### Setup

1. Clone the repository:
```bash
git clone https://github.com/YOUR_USER/freefirebot.git
cd freefirebot
```

2. Set environment variables:
```bash
export BOT_TOKEN=your_bot_token
export BOT_USERNAME=your_bot_username
```

3. Build and run:
```bash
mvn clean package -DskipTests
java -jar target/freefirebot-0.0.1-SNAPSHOT.jar
```

### Docker

```bash
docker build -t ff-bot .
docker run -d -e BOT_TOKEN=your_token -e BOT_USERNAME=your_username ff-bot
```

## 📁 Project Structure

```
com.devlil0.freefirebot
├── bot/                → Telegram bot & config
├── service/            → API communication (WebClient)
├── model/dto/          → Data Transfer Objects
└── helper/             → Utility classes
```

## 📌 Commands

| Command | Description |
|---------|-------------|
| `/start` | Welcome message and command list |
| `/2138152569>` | Check ban status of a Free Fire account |
| `/player <2138152569>` | Get player profile information |

## 🤝 Contributing

Feel free to fork, open issues, or submit pull requests.

## 📄 License

This project is for educational purposes only. Not affiliated with Garena or Free Fire.
