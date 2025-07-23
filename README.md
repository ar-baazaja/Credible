# Credible Frontend

This repository contains the **frontend** of the Credible app—a modern Flutter application for managing and showcasing your projects and portfolios with seamless GitHub and LinkedIn integration, and AI-powered portfolio generation.

---

## Table of Contents
- [Overview](#overview)
- [Screenshots](#screenshots)
- [Features](#features)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Ollama Setup Guide](#ollama-setup-guide)
- [GitHub Setup Guide](#github-setup-guide)
- [Architecture](#architecture)
- [Theme](#theme)
- [Dependencies](#dependencies)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

---

## Overview
Credible is a cross-platform Flutter app that helps users:
- Upload projects to GitHub and LinkedIn
- Generate professional portfolios from a CV or manual input
- Use local AI (Ollama) for content generation
- Enjoy a modern, dark-themed UI

## Screenshots

| Home Screen | Upload Project | Portfolio Generator | Settings |
|-------------|---------------|--------------------|----------|
| ![Home](WhatsApp%20Image%202025-07-14%20at%205.53.53%20AM%20(1).jpeg) | ![Upload](WhatsApp%20Image%202025-07-14%20at%205.54.04%20AM%20(1).jpeg) | ![Portfolio](WhatsApp%20Image%202025-07-14%20at%205.54.23%20AM%20(1).jpeg) | ![Settings](WhatsApp%20Image%202025-07-14%20at%205.56.08%20AM%20(1).jpeg) |

## Features
- **Project Upload:** Create GitHub repos and add projects to LinkedIn
- **Portfolio Generator:** Build a portfolio website from your CV or details
- **Settings:** Manage API keys and service connections
- **AI-Powered Content:** Uses Ollama for project/portfolio text
- **Modern UI:** Dark theme, orange accent, responsive design

## Setup Instructions

### Prerequisites
1. **Flutter SDK:** v3.8.1 or higher
2. **Ollama:** Local AI service (see [Ollama Setup Guide](#ollama-setup-guide))
3. **GitHub Token:** [Create one here](https://github.com/settings/tokens) (`repo`, `workflow` scopes)
4. **LinkedIn Access Token:** From LinkedIn Developer Console

### Installation
```bash
git clone https://github.com/ar-baazaja/Credible.git
cd my_app
flutter pub get
```

### Environment Setup
Create a `.env` file in the root directory:
```env
GITHUB_TOKEN=your_github_token_here
LINKEDIN_ACCESS_TOKEN=your_linkedin_token_here
OLLAMA_URL=http://localhost:11434
```

### Run the App
```bash
flutter run
```

## Usage
### Project Upload
- Go to **Upload** tab
- Fill in project details (name, type, description, tech, dates)
- Choose upload options (GitHub, LinkedIn, private)
- Click **Upload Project**

### Portfolio Generation
- Go to **Portfolio** tab
- (Optional) Upload your CV
- Fill in portfolio details
- Choose a template
- Click **Generate Portfolio**

### Settings
- Go to **Settings** tab
- Enter API keys and service URLs
- Test connections and save

---

## Ollama Setup Guide
- Install Ollama: https://ollama.ai/
- Run: `ollama serve`
- Pull a model: `ollama pull llama2`
- For Android: set `OLLAMA_HOST=0.0.0.0:11434` and use your computer's IP in the app settings
- For remote access: use [ngrok](https://ngrok.com/) or similar
- See `my_app/README_OLLAMA_SETUP.md` for full details

## GitHub Setup Guide
- Create a personal access token ([guide](my_app/GITHUB_SETUP.md))
- Scopes: `repo`, `user`, `read:user`
- Add token in app settings and test connection

---

## Architecture
- **Services:** OllamaService, GitHubService, LinkedInService
- **UI:** HomeScreen, ProjectUploadScreen, PortfolioScreen, SettingsScreen
- **State:** Uses Provider/StatefulWidgets (see code)

## Theme
- Background: `#111111`
- Surface: `#1A1A1A`
- Primary: `#FF7A00`
- Secondary: `#FFC000`
- Text: `#F8F8F8`
- Font: Inter, Poppins, SF Pro
- Rounded corners: 16px
- Soft shadows, consistent spacing

## Dependencies
- See [`pubspec.yaml`](my_app/pubspec.yaml) for full list
- Highlights: `http`, `dio`, `file_picker`, `webview_flutter`, `shared_preferences`, `url_launcher`, `flutter_svg`, `lottie`, `shimmer`

## Troubleshooting
- **Ollama:** Ensure running, correct URL, model pulled
- **GitHub:** Token must have correct scopes, not expired
- **LinkedIn:** Use valid access token
- **Portfolio:** Supported CV formats: PDF, DOC, DOCX, TXT
- See [my_app/README.md](my_app/README.md) for more

## Contributing
- Linting: Uses `flutter_lints` (see `analysis_options.yaml`)
- Run `flutter analyze` before submitting PRs
- Fork, branch, PR, and test thoroughly

## License
This project is licensed under the MIT License.

## Support
- Create an issue on GitHub
- Check troubleshooting above
- Ensure all prerequisites are met

---

**Credible Frontend** — Modern project & portfolio management, powered by Flutter and AI. 