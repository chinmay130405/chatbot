# Groq AI Chatbot

A beautiful, modern chatbot built with React and powered by Groq AI's lightning-fast LLM inference.

## Features

✨ **Modern UI Design** - Clean, responsive interface with smooth animations
🚀 **Fast Responses** - Powered by Groq's ultra-fast inference
💬 **Real-time Chat** - Smooth message flow with typing indicators
🎨 **Beautiful Gradients** - Eye-catching purple gradient theme
📱 **Responsive** - Works great on desktop and mobile devices
🔒 **Secure** - API key is stored in browser memory only

## Prerequisites

- Node.js (v14 or higher)
- A Groq API key (get one free at https://console.groq.com/keys)

## Installation

1. Navigate to the project directory:
```bash
cd groq-chatbot
```

2. Install dependencies:
```bash
npm install
```

3. Set up your Groq API key:
   - Create a `.env` file in the root directory (copy from `.env.example`)
   - Get your free API key from [Groq Console](https://console.groq.com/keys)
   - Add your API key to `.env`:
   ```
   VITE_GROQ_API_KEY=your_actual_api_key_here
   ```

4. Start the development server:
```bash
npm run dev
```

5. Open your browser and go to `http://localhost:5173`

## Usage

**Option 1: Using .env file (Recommended)**
- Add your API key to the `.env` file as shown above
- The app will automatically use it and skip the API key input screen

**Option 2: Manual entry**
- If no API key is set in `.env`, you'll be prompted to enter it when you first open the app
- You can change your API key anytime by clicking the 🔑 button in the header

## Tech Stack

- **React** - UI library
- **Vite** - Build tool and dev server
- **Groq SDK** - For AI inference
- **CSS3** - Styling with gradients and animations

## Models

This chatbot uses the `llama3-8b-8192` model from Groq, which provides:
- Fast inference times (< 1 second)
- High-quality responses
- Large context window (8192 tokens)

## Building for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

## Preview Production Build

```bash
npm run preview
```

## Note

The API key is stored in browser memory and is never sent to any server except Groq's API. The `dangerouslyAllowBrowser: true` flag is used to enable client-side API calls. For production applications, consider implementing a backend proxy to keep your API key secure.

## License

MIT
