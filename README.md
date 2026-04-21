# ☁️ Cloudyte Drive Bot

Professional Telegram Bot for Google Drive Management

## Features

- **Multiple Drive Accounts** - Connect and manage unlimited Google Drive accounts
- **File Browser** - Browse files and folders with intuitive navigation
- **File Upload** - Upload files from Telegram directly to Drive
- **File Download** - Download files from Drive to Telegram (up to 20MB)
- **Search** - Search across all your files quickly
- **Share Links** - Generate public shareable links instantly
- **Storage Info** - Monitor your Drive storage usage
- **File Operations** - Delete files, open folders, organize content

## Quick Start

### Prerequisites

- Python 3.9+
- MongoDB
- Telegram Bot Token
- Google Cloud Project with Drive API enabled

### Installation

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd cloudyte
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Configure environment:
   ```bash
   cp .env.example .env
   # Edit .env with your credentials
   ```

4. Run the bot:
   ```bash
   python main.py
   ```

## Configuration

### Environment Variables

```env
BOT_TOKEN=your_telegram_bot_token
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
REDIRECT_URI=https://your-domain.com/oauth_callback
MONGO_URI=mongodb://localhost:27017
PORT=3000
```

### Google Cloud Setup

1. Create a project in [Google Cloud Console](https://console.cloud.google.com/)
2. Enable Google Drive API
3. Create OAuth 2.0 credentials (Web application)
4. Add authorized redirect URI: `https://your-domain.com/oauth_callback`
5. Configure OAuth consent screen with Drive scopes

## Bot Commands

| Command | Description |
|---------|-------------|
| `/start` | Start the bot |
| `/files` | Browse your Drive files |
| `/upload` | Upload file from Telegram |
| `/search` | Search files |
| `/storage` | View storage information |
| `/addaccount` | Add Drive account |
| `/settings` | Manage accounts |

## Usage

1. **Connect Drive**: Use `/addaccount` to connect your Google Drive
2. **Browse Files**: Use `/files` to see your files and folders
3. **Upload**: Use `/upload` and send any file
4. **Download**: Click "⬇️ Download" on any file
5. **Search**: Use `/search` and type your query
6. **Share**: Click "🔗 Share" to get a public link

## Deployment

Works with:
- Coolify (recommended)
- Docker
- Any VPS with Python 3.9+

See Rexify's DEPLOYMENT.md for detailed deployment instructions (same process).

## Security

- OAuth tokens encrypted in MongoDB
- HTTPS required for OAuth callbacks
- File content never stored permanently
- Users control all file operations



## Support

For issues and questions, open an issue on GitHub.

---

**Made with ❤️ for seamless Drive management**
