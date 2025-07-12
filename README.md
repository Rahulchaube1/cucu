# 🤖 Cucu - AI WhatsApp Assistant

<div align="center">

![Cucu Logo](https://img.shields.io/badge/🤖-Cucu-brightgreen?style=for-the-badge)
[![GitHub Stars](https://img.shields.io/github/stars/Rahulchaube1/cucu?style=for-the-badge)](https://github.com/Rahulchaube1/cucu/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Rahulchaube1/cucu?style=for-the-badge)](https://github.com/Rahulchaube1/cucu/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Docker](https://img.shields.io/badge/Docker-Ready-blue?style=for-the-badge&logo=docker)](https://hub.docker.com/)

**🚀 The Ultimate AI-Powered WhatsApp Assistant**

*Bringing the power of OpenAI GPT and DALL-E directly to your WhatsApp conversations*

[✨ Features](#-features) •
[🚀 Quick Start](#-quick-start) •
[📖 Documentation](#-documentation) •
[🤝 Contributing](#-contributing) •
[⭐ Star Us](#-star-us)

</div>

---

## 🎯 What is Cucu?

Cucu is an intelligent WhatsApp assistant that transforms your messaging experience with cutting-edge AI capabilities. Cucu can engage in meaningful conversations, generate stunning images, transcribe voice messages, and even search the web - all through WhatsApp!

### 🌟 Created by Rahul Chaube

This project is lovingly crafted and maintained by **Rahul Chaube**, bringing advanced AI capabilities to everyday messaging.

---

## ✨ Features

### 🧠 **Intelligent Conversations**
- **Natural Language Processing**: Powered by OpenAI GPT models for human-like conversations
- **Context Awareness**: Maintains conversation history for better responses
- **Multi-language Support**: Communicate in multiple languages

### 🎨 **Image Generation**
- **DALL-E Integration**: Generate stunning images from text descriptions
- **Creative Art**: Create logos, artwork, and illustrations instantly
- **Custom Styles**: Request specific artistic styles and themes

### 🎤 **Voice Message Support**
- **Speech Recognition**: Transcribe voice messages to text
- **Voice Responses**: Convert text responses back to voice
- **Multi-format Support**: Handle various audio formats

### 🌐 **Web Search Integration**
- **Real-time Information**: Get current news and information
- **SerpAPI Integration**: Powerful web search capabilities
- **Fact Checking**: Verify information with web sources

### 🔧 **Advanced Features**
- **Docker Support**: Easy deployment with containerization
- **Prefix Commands**: Customize bot activation with prefixes
- **Session Management**: Persistent WhatsApp sessions
- **Error Handling**: Robust error management and recovery

---

## 🚀 Quick Start

### Prerequisites

- Node.js (18 or newer)
- npm or yarn
- OpenAI API key ([Get one here](https://beta.openai.com/signup))
- WhatsApp account

### 🐳 Docker Installation (Recommended)

```bash
# Clone the repository
git clone https://github.com/Rahulchaube1/cucu.git
cd cucu

# Configure environment variables
cp .env-example .env
# Edit .env with your API keys

# Run with Docker Compose
docker-compose up -d
```

### 💻 Manual Installation

```bash
# Clone and install
git clone https://github.com/Rahulchaube1/cucu.git
cd cucu
npm install

# Configure environment
cp .env-example .env
# Edit .env with your API keys

# Start the bot
npm start
```

### 🎯 Quick Setup Scripts

#### Windows
```powershell
# Run the automated installer
.\install.bat
```

#### Linux/Mac
```bash
# Run the automated installer
chmod +x install.sh
./install.sh
```

---

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
# OpenAI Configuration
OPENAI_API_KEY=your_openai_api_key_here
OPENAI_GPT_MODEL=gpt-3.5-turbo

# Optional: Enable prefix mode
PREFIX_ENABLED=true

# Optional: Web search capability
SERPAPI_API_KEY=your_serpapi_key_here
```

### API Keys Setup

1. **OpenAI API Key**: 
   - Visit [OpenAI Platform](https://beta.openai.com/signup)
   - Create an account and generate an API key
   - Add billing information for usage

2. **SerpAPI Key** (Optional):
   - Visit [SerpAPI](https://serpapi.com/)
   - Sign up for web search capabilities
   - Get your API key from the dashboard

---

## 📱 Usage

### Basic Commands

Once Cucu is running:

1. **Scan QR Code**: Use your WhatsApp to scan the QR code displayed in the terminal
2. **Start Chatting**: Send messages to your WhatsApp number
3. **Generate Images**: Ask Cucu to create images: "Generate an image of a sunset over mountains"
4. **Voice Messages**: Send voice messages for transcription and response
5. **Web Search**: Ask for current information: "What's the latest news about AI?"

### Example Conversations

```
You: "Create an image of a robot playing guitar"
Cucu: [Generates and sends beautiful AI artwork]

You: "What's the weather like today?"
Cucu: [Searches web and provides current weather information]

You: [Voice message: "Tell me a joke"]
Cucu: [Transcribes voice and responds with a funny joke]
```

---

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   WhatsApp      │    │      Cucu       │    │     OpenAI      │
│   Web Client    │◄──►│   AI Assistant  │◄──►│   API Service   │
└─────────────────┘    └─────────────────┘    └─────────────────┘
                              │
                              ▼
                       ┌─────────────────┐
                       │   Web Search    │
                       │   (SerpAPI)     │
                       └─────────────────┘
```

---

## 🛠️ Development

### Project Structure

```
cucu/
├── src/
│   ├── handlers/          # Message handlers
│   ├── services/          # AI and web services
│   ├── utils/             # Utility functions
│   └── config/            # Configuration files
├── docs/                  # Documentation
├── .github/               # GitHub templates and workflows
├── docker-compose.yml     # Docker configuration
├── Dockerfile            # Container setup
└── package.json          # Project dependencies
```

### Contributing

We welcome contributions! Please read our [Contributing Guide](CONTRIBUTING.md) for details on:

- 🐛 Bug reports
- 💡 Feature requests
- 🔧 Code contributions
- 📚 Documentation improvements

### Development Setup

```bash
# Clone and setup
git clone https://github.com/Rahulchaube1/cucu.git
cd cucu
npm install

# Development mode
npm run dev

# Testing
npm test

# Build
npm run build
```

---

## 📊 Performance & Scaling

### Resource Usage
- **Memory**: ~100-200MB base usage
- **CPU**: Low usage during idle, spikes during AI processing
- **Storage**: Session data and logs (~10-50MB)

### Scaling Considerations
- **Rate Limits**: OpenAI API has rate limits
- **Concurrent Users**: Handles multiple conversations
- **Session Management**: Persistent WhatsApp sessions

---

## 🔒 Security & Privacy

### Data Protection
- **No Message Storage**: Messages are not permanently stored
- **API Key Security**: Environment variables for sensitive data
- **Session Encryption**: WhatsApp sessions are securely managed

### Best Practices
- Use strong API keys
- Regularly rotate credentials
- Monitor usage and costs
- Review conversation logs

---

## 💰 Cost Management

### OpenAI Pricing
- **GPT-3.5-turbo**: ~$0.002 per 1K tokens
- **DALL-E**: ~$0.020 per image
- **Whisper**: ~$0.006 per minute

### Cost Optimization
- Set usage limits in OpenAI dashboard
- Monitor token usage
- Use efficient prompts
- Implement user rate limiting

---

## 🚀 Deployment

### Docker Deployment
```bash
# Build and run
docker-compose up -d

# View logs
docker-compose logs -f

# Stop
docker-compose down
```

### Cloud Deployment
- **AWS**: EC2 instance with Docker
- **Google Cloud**: Compute Engine or Cloud Run
- **Azure**: Container Instances
- **Heroku**: Container deployment

---

## 🤝 Community

### Support
- 📧 **Email**: rahulchaube1@gmail.com
- 💬 **Issues**: [GitHub Issues](https://github.com/Rahulchaube1/cucu/issues)
- 📖 **Wiki**: [Project Wiki](https://github.com/Rahulchaube1/cucu/wiki)

### Contributing
- 🐛 Report bugs
- 💡 Suggest features
- 🔧 Submit pull requests
- 📚 Improve documentation

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **OpenAI** for providing amazing AI capabilities
- **WhatsApp Web.js** for WhatsApp integration
- **SerpAPI** for web search functionality
- **Docker** for containerization support
- **Open Source Community** for inspiration and support

---

## ⭐ Star Us

If you find Cucu helpful, please give us a star! It helps others discover this project.

[![GitHub Stars](https://img.shields.io/github/stars/Rahulchaube1/cucu?style=social)](https://github.com/Rahulchaube1/cucu/stargazers)

---

<div align="center">

**Made  by [Rahul Chaube](https://github.com/Rahulchaube1)**

*Bringing AI to your conversations, one message at a time*

[⬆️ Back to Top](#-cucu---ai-whatsapp-assistant)

</div>
