# Music Assistant Alexa API Addon

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports i386 Architecture][i386-shield]

This addon provides an API bridge between Music Assistant and Alexa skills, allowing you to control your music through voice commands.

## Installation

1. Add this repository to your Home Assistant addon store: `https://github.com/mcinnes01/music-assistant-alexa-api`
2. Install the "Music Assistant Alexa API Addon" addon
3. Configure the addon with your credentials
4. Start the addon

## Configuration

```yaml
username: your_username
password: your_password
port: 3000
```

### Option: `username`

The username for authentication (optional).

### Option: `password`

The password for authentication (optional).

### Option: `port`

The port number for the API endpoint (default: 3000).

## API Endpoints

### POST `/ma/push-url`

Music Assistant calls this endpoint to push stream URLs.

**Body:**
```json
{
  "streamUrl": "https://example.com/stream.mp3",
  "title": "Song Title",
  "artist": "Artist Name",
  "album": "Album Name",
  "imageUrl": "https://example.com/cover.jpg"
}
```

### GET `/ma/latest-url`

Alexa skill calls this endpoint to get the latest stream URL.

**Response:**
```json
{
  "streamUrl": "https://example.com/stream.mp3",
  "title": "Song Title",
  "artist": "Artist Name",
  "album": "Album Name",
  "imageUrl": "https://example.com/cover.jpg"
}
```

## Support

Got questions?

You have several options to get them answered:

- The [Home Assistant Community Forum][forum]
- Open an issue on our [GitHub repository][repository]

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[forum]: https://community.home-assistant.io
[repository]: https://github.com/mcinnes01/music-assistant-alexa-api