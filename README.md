# Code Review AI Assistant 🪄

A lightweight, visually polished, single-page web application that provides AI-powered code reviews. It uses Google's Gemini API (with a built-in local simulation fallback) to analyze code snippets, highlight positive aspects, and suggest actionable improvements with side-by-side diffs.

## ✨ Features

- **Live Gemini API Integration:** Connect your Google AI Studio API key to perform live code reviews using models like `gemini-1.5-flash`, `gemini-1.5-pro`, or any custom model.
- **Simulation Mode:** No API key? No problem. The app features a built-in heuristic simulation engine that analyzes pre-loaded suboptimal code templates entirely offline.
- **Customizable System Prompt:** Edit the underlying LLM instructions directly in the UI to tailor the review focus (e.g., performance, security, readability).
- **Multi-Language Support:** Preloaded code snippets for Python, JavaScript, C++, and SQL, along with a "Custom Code" option.
- **Visual & Raw Output:** Toggle between a beautifully styled visual review (complete with diff syntax highlighting) and raw Markdown output.
- **Privacy-First Local Storage:** Your API key and custom settings are saved exclusively in your browser's `localStorage`—they are never sent anywhere except directly to Google's generative language endpoints.

## 🛠️ Technologies Used

- **HTML5, CSS3, Vanilla JavaScript:** No build steps or heavy frameworks required.
- **[Marked.js](https://marked.js.org/):** For rendering the LLM's Markdown output into HTML.
- **[Prism.js](https://prismjs.com/):** For syntax highlighting in the Raw Markdown view.
- **[FontAwesome](https://fontawesome.com/):** For elegant iconography.
- **Google Fonts:** Utilizing *Outfit*, *Plus Jakarta Sans*, and *JetBrains Mono* for a modern, developer-focused aesthetic.

## 🚀 Getting Started

1. **Download/Clone:** Download the `index.html` file to your local machine.
2. **Open the App:** Simply double-click `index.html` to open it in any modern web browser. No server setup is required.
3. **Try Simulation Mode:** - Select a language (e.g., Python).
   - Click **Analyze Code Snippet**.
   - View the generated review in the "Visual Review" tab.

## ⚙️ Configuring the Live API

To analyze your own custom code snippets, you need to provide a free Gemini API key:

1. Get a free API key from [Google AI Studio](https://aistudio.google.com/).
2. In the app, click the **Settings (Gear) icon** in the top right corner.
3. Paste your API key into the input field and click **Verify Key**.
4. Select your preferred model (e.g., `gemini-1.5-flash`) or enter a custom model name.
5. Click **Save Changes**. The badge will update to "Live API Mode".
6. Select **Custom Code**, paste your code, and click **Analyze Code Snippet**!

## 🎨 UI/UX Highlights

- **Glassmorphism Design:** Modern UI with blurred backdrops, glowing accents, and dark-mode aesthetic.
- **Responsive Layout:** Works smoothly on desktop and scales down for smaller screens.
- **Interactive Diff Viewer:** Clearly displays recommended code changes with distinct color-coding for insertions and deletions.
- **Toast Notifications:** Unobtrusive alerts for copying prompts, verifying keys, and saving settings.

## 📝 Modifying the Prompt

You can customize how the AI reviews your code by expanding the **Edit Review System Prompt** accordion on the left panel. Be sure to keep the expected formatting rules intact so the Visual Review parser works correctly!
