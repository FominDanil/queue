# Queue Bot

This is a project for sending messages with a queue on a Telegram chats. Users can join the queue by clicking on a button and the queue will be completed in a day or by clicking on another button. The application uses Python, aiogram, and Redis. The entire project can be spun up using Docker Compose.

## Requirements
- Python 3.10
- Docker and Docker Compose
- Telegram bot api token

## Installation

First, you need to clone this repository:

```bash
git clone https://github.com/FominDanil/queue.git
cd queue
```

## Configuration
### .env
The application uses environment variables for configuration. Rename `.env.example` to `.env` and fill in the necessary details:

```bash
cp .env.example .env
nano .env
```

- TOKEN: get it from @BotFather
- TIME_ZONE: Your time zone, by default it's 'Europe/Moscow'

## Usage

Once you have your environment variables set up, you can start the application using Docker Compose:

```bash
docker-compose up -d --build
```

The application will now run in the background, managing the queue and sending messages in your Telegram channel according to the settings defined in the configuration.


### Create queue
1. While in the chat, write
```
@your_bot_name Title_to_queue
```

2. Choose one of the options: automatic completion or completion by button
![Imgur](https://i.imgur.com/xm5NlaE.jpg)
3. Сlick on the first button to take a place in the queue
![Imgur](https://i.imgur.com/rvLbH5O.jpg)
4. Now you are added to the queue
![Imgur](https://i.imgur.com/8KKWRAG.jpg)
5. Click on the second button to close the queue
![Imgur](https://i.imgur.com/WR8Gpv6.jpg)
