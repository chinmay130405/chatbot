# 🤖 Groq AI Chatbot

A beautiful, modern chatbot built with **React** and powered by **Groq AI's** lightning-fast LLM inference using the **Llama 3.1** model.

![React](https://img.shields.io/badge/React-18.3.1-blue?logo=react) ![Groq](https://img.shields.io/badge/Groq-AI-orange) ![Vite](https://img.shields.io/badge/Vite-5.4.2-purple?logo=vite) ![License](https://img.shields.io/badge/License-MIT-green)

## ✨ Features

- 🎨 **Modern UI Design** - Clean, responsive interface with smooth animations
- ⚡ **Ultra-Fast Responses** - Powered by Groq's lightning-fast inference engine
- 💬 **Real-time Chat** - Smooth message flow with animated typing indicators
- � **Beautiful Gradients** - Eye-catching purple gradient theme
- 📱 **Fully Responsive** - Works seamlessly on desktop, tablet, and mobile devices
- 🔒 **Secure** - Environment-based API key management
- 🎯 **Latest AI Model** - Uses Llama 3.1-8B Instant for optimal performance

## 🚀 Quick Start

### Prerequisites

Before you begin, make sure you have:
- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js)
- A **Groq API key** - [Get one free here](https://console.groq.com/keys)

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/chinmay130405/chatbot.git
   cd chatbot
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up your API key**
   
   Create a `.env` file in the root directory:
   ```bash
   # On Windows (PowerShell)
   Copy-Item .env.example .env
   
   # On Mac/Linux
   cp .env.example .env
   ```
   
   Open the `.env` file and add your Groq API key:
   ```env
   VITE_GROQ_API_KEY=your_groq_api_key_here
   ```
   
   > **⚠️ Important:** Never commit your `.env` file to Git! It's already in `.gitignore`.

4. **Get your Groq API key**
   - Visit [console.groq.com/keys](https://console.groq.com/keys)
   - Sign up or log in (it's completely free!)
   - Click "Create API Key"
   - Copy the key and paste it in your `.env` file

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   
   Navigate to the URL shown in your terminal (usually `http://localhost:5173`)

🎉 **That's it!** Your chatbot is now running!

## 📁 Project Structure

```
chatbot/
├── src/
│   ├── components/
│   │   ├── Chatbot.jsx          # Main chatbot component
│   │   └── Chatbot.css          # Chatbot styling
│   ├── App.jsx                  # Root component
│   ├── App.css                  # App styling
│   ├── main.jsx                 # Entry point
│   └── index.css                # Global styles
├── .env.example                 # Environment variables template
├── .gitignore                   # Git ignore rules
├── CONTRIBUTING.md              # Contributing guidelines
├── index.html                   # HTML template
├── package.json                 # Dependencies and scripts
├── vite.config.js               # Vite configuration
└── README.md                    # This file
```

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| [React](https://react.dev/) | UI library for building the interface |
| [Vite](https://vitejs.dev/) | Lightning-fast build tool and dev server |
| [Groq SDK](https://www.npmjs.com/package/groq-sdk) | AI inference with Groq's API |
| CSS3 | Custom styling with gradients and animations |

## 🤖 AI Model

This chatbot uses **Llama 3.1-8B Instant** from Groq, which provides:
- ⚡ **Ultra-fast inference** - Responses in milliseconds
- 🎯 **High-quality responses** - Natural language understanding
- 💡 **8B parameters** - Efficient yet powerful
- 📝 **Large context window** - Better conversation flow

### Available Models

You can change the model in `src/components/Chatbot.jsx`:

```javascript
model: 'llama-3.1-8b-instant', // Change this line
```

Other available Groq models:
- `llama-3.1-8b-instant` (current - fastest)
- `llama-3.1-70b-versatile` (more capable)
- `mixtral-8x7b-32768` (largest context window)

## 📦 Available Scripts

### `npm run dev`
Starts the development server with hot reload
- URL: `http://localhost:5173`

### `npm run build`
Builds the app for production to the `dist` folder
- Optimized and minified
- Ready for deployment

### `npm run preview`
Preview the production build locally
- Test before deploying

## 🌐 Deployment

### Option 1: Vercel (Recommended)

1. Push your code to GitHub
2. Import your repository on [Vercel](https://vercel.com)
3. Add environment variable:
   - Name: `VITE_GROQ_API_KEY`
   - Value: Your Groq API key
4. Deploy!

### Option 2: Netlify

1. Build the project: `npm run build`
2. Drag and drop the `dist` folder to [Netlify](https://netlify.com)
3. Add environment variable in Site Settings:
   - Key: `VITE_GROQ_API_KEY`
   - Value: Your Groq API key

### Option 3: GitHub Pages

1. Install gh-pages: `npm install --save-dev gh-pages`
2. Add to `package.json`:
   ```json
   "homepage": "https://chinmay130405.github.io/chatbot",
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```
3. Run: `npm run deploy`

> **⚠️ Security Note:** For production, consider implementing a backend proxy to keep your API key secure. The current setup uses `dangerouslyAllowBrowser: true` which exposes the API key in client-side code.

## 🐛 Troubleshooting

### API Key Not Working
- ✅ Ensure `.env` file is in the root directory
- ✅ Verify the key has the `VITE_` prefix: `VITE_GROQ_API_KEY`
- ✅ Check that there are NO quotes around the API key value
- ✅ Restart the dev server after changing `.env`

### "Missing script: dev" Error
- ✅ Make sure you're in the correct directory
- ✅ Verify `package.json` exists
- ✅ Run `npm install` first

### Port Already in Use
- ✅ Vite will automatically try the next available port (5174, 5175, etc.)
- ✅ Check your terminal for the actual port being used

### Build Errors
- ✅ Delete `node_modules` and `package-lock.json`
- ✅ Run `npm install` again
- ✅ Make sure you're using Node.js v14 or higher

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Ways to contribute:
- 🐛 Report bugs
- 💡 Suggest new features
- 📝 Improve documentation
- 🔧 Submit pull requests

## 📄 License

This project is licensed under the MIT License - feel free to use it for personal or commercial projects!

## 🙏 Acknowledgments

- [Groq](https://groq.com/) - For their incredible AI inference platform
- [Meta AI](https://ai.meta.com/) - For the Llama 3.1 model
- [React Team](https://react.dev/) - For the amazing UI library

## 📧 Support

If you have any questions or run into issues:

1. Check the [Troubleshooting](#-troubleshooting) section
2. Open an issue on GitHub
3. Visit [Groq's documentation](https://console.groq.com/docs)

## 🌟 Show Your Support

If you found this project helpful, please give it a ⭐ on GitHub!

---

**Made with ❤️ using React and Groq AI**
