# AudioPod AI Documentation

This repository contains the comprehensive API documentation for AudioPod AI - the leading platform for AI-powered audio processing, speech synthesis, music generation, and more.

## 📚 Documentation Overview

This documentation covers AudioPod AI's complete suite of APIs:

### 🎯 Core Services
- **Text-to-Speech** - Advanced speech synthesis with custom voice cloning
- **Speech-to-Text** - High-accuracy transcription with speaker diarization
- **Music Generation** - AI-powered music creation from text prompts
- **Voice Management** - Custom voice training and management

### 🔧 Audio Processing
- **Voice Changer** - Real-time voice transformation and conversion
- **Stem Separation** - Isolate instruments and vocals from audio
- **Noise Reduction** - Advanced audio cleaning and enhancement
- **Speaker Separation** - Extract individual speakers from audio

### 🌐 Content & Media
- **Media Extraction** - Download audio/video from online platforms
- **Speech Translation** - End-to-end speech-to-speech translation
- **AI Dubbing** - Voice cloning with translation capabilities

### 👤 Account & Billing
- **Authentication** - JWT tokens, API keys, and OAuth integration
- **Credit Management** - Usage tracking and pay-as-you-go billing
- **Account Management** - User profiles and subscription handling

## 🚀 Getting Started

### Quick Links
- **[AudioPod AI Dashboard](https://www.audiopod.ai/dashboard)** - Manage your account and API keys
- **[Live Documentation](https://docs.audiopod.ai)** - Latest published documentation
- **[API Status](https://api.audiopod.ai/health)** - Service health and uptime
- **[Pricing](https://www.audiopod.ai/pricing)** - Credit costs and subscription plans

### New to AudioPod AI?
1. **[Create Account](https://www.audiopod.ai/auth/signup)** - Get 10,000 free credits
2. **[Generate API Key](https://www.audiopod.ai/dashboard/account/api-keys)** - For programmatic access
3. **[Follow Quickstart Guide](/quickstart)** - Make your first API call
4. **[Choose Your SDK](https://github.com/audiopod-ai)** - Python, Node.js, and more

## 🛠 Development

### Local Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview documentation changes locally:

```bash
# Install Mintlify CLI
npm i -g mint

# Navigate to documentation directory
cd ap_docs

# Start local development server
mint dev
```

View your local preview at `http://localhost:3000`.

### Making Changes

1. **API Reference Updates**: Edit files in `/api-reference/`
2. **Account Guides**: Edit files in `/account/`
3. **Navigation**: Update `docs.json` for menu structure
4. **Styling**: Modify theme settings in `docs.json`

### Testing Changes

Before submitting changes:
```bash
# Check for syntax errors
mint build

# Validate all links
mint check-links

# Run accessibility checks
mint a11y-check
```

## 📖 Documentation Structure

```
ap_docs/
├── index.mdx                 # Homepage
├── quickstart.mdx           # Getting started guide
├── authentication.mdx       # Auth overview
├── account/                 # Account management
│   ├── registration.mdx
│   ├── api-keys.mdx
│   └── credits.mdx
├── api-reference/          # API documentation
│   ├── auth.mdx           # Authentication endpoints
│   ├── text-to-speech.mdx
│   ├── music-generation.mdx
│   ├── voice-management.mdx
│   └── ...
└── docs.json              # Navigation & config
```

## 🔄 Publishing

Documentation is automatically deployed when changes are pushed to the main branch. The deployment process:

1. **Automatic Build**: GitHub Actions builds the documentation
2. **Validation**: Checks for broken links and syntax errors  
3. **Deploy**: Updates live at [docs.audiopod.ai](https://docs.audiopod.ai)
4. **CDN Refresh**: Global content distribution update

## 📝 Contributing

### Guidelines
- **Clear Examples**: Include working code samples for all endpoints
- **Error Handling**: Document common errors and solutions
- **SDK Integration**: Show examples in multiple languages
- **Real Use Cases**: Provide practical implementation examples

### Code Examples
- Use actual AudioPod AI service names and endpoints
- Include proper error handling
- Show both simple and advanced usage
- Test all code examples before submitting

### Style Guide
- **Headers**: Use clear, descriptive section titles
- **Parameters**: Document all request/response fields
- **Status Codes**: Include HTTP status codes and meanings
- **Rate Limits**: Note any usage limitations

## 🐛 Issues & Support

### Documentation Issues
- **Bug Reports**: [Create GitHub Issue](https://github.com/audiopod-ai/docs/issues)
- **Feature Requests**: [Submit Enhancement](https://github.com/audiopod-ai/docs/issues/new)
- **Content Errors**: Use "Edit on GitHub" link on any page

### API Support
- **Technical Support**: [support@audiopod.ai](mailto:support@audiopod.ai)
- **Community Forum**: [Discord Community](https://discord.gg/audiopod)
- **Status Updates**: [@AudioPodAI](https://twitter.com/AudioPodAI) on Twitter

## 🏗 Technical Stack

- **Framework**: [Mintlify](https://mintlify.com) - Modern documentation platform
- **Hosting**: Vercel with global CDN
- **Version Control**: Git with automatic deployments
- **Analytics**: Built-in usage tracking and search analytics

## 📄 License

This documentation is licensed under [MIT License](LICENSE). The AudioPod AI API itself is a commercial service - see [Terms of Service](https://www.audiopod.ai/terms) for usage terms.
