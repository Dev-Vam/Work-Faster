# 🕒 Work Faster – A Cute Pomodoro Timer App

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A beautiful and functional Pomodoro timer desktop application built with **React**, **TypeScript**, and **Electron.js**.

**Author:** Dev-Vamerlen <merlenvam@proton.me>

---

## ✨ Features

- 🎨 Beautiful gradient UI with smooth transitions
- ⏱️ Customizable work and break durations
- 🔔 Sound notification when timer completes
- 💼 Switch between Work and Break modes
- 🖥️ Cross-platform desktop app (Windows, macOS, Linux)
- 🎯 Clean and minimalist design
- ⚡ Lightweight and fast

---

## 🚀 Quick Start

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- npm (comes with Node.js)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/work-faster.git
cd work-faster
```

2. **Install dependencies**
```bash
npm install
```

3. **Install additional development dependencies**
```bash
npm install --save-dev electron electron-builder concurrently wait-on electron-is-dev
```

---

## 🛠️ Development

### Run in Development Mode

```bash
npm run electron-dev
```

This will start the React development server and open the Electron app with hot-reloading enabled.

### Run React Only (Browser)

```bash
npm start
```

Opens the app in your default browser at `http://localhost:3000`

---

## 📦 Building for Production

### Build for Windows

```bash
npm run dist
```

This creates:
- **NSIS Installer** (`.exe`) - Full installer with start menu shortcuts
- **Portable Executable** (`.exe`) - No installation required

The built files will be in the `dist` folder.

### Build for All Platforms

```bash
npm run electron-build
```

---

## 📂 Project Structure

```
work-faster/
├── public/
│   ├── electron.js          # Electron main process
│   ├── index.html
│   └── icon.png             # App icon
├── src/
│   ├── App.tsx              # Main React component
│   ├── App.css              # Styling
│   ├── index.tsx
│   └── react-app-env.d.ts
├── package.json             # Dependencies and scripts
├── tsconfig.json            # TypeScript configuration
└── README.md
```

---

## 🎮 How to Use

1. **Choose Mode**: Click "Work" or "Break" to select your timer mode
2. **Set Duration**: Adjust work and break durations in minutes
3. **Start Timer**: Click the "▶️ Start" button to begin
4. **Pause/Resume**: Click "⏸️ Pause" to pause the timer
5. **Reset**: Click "🔄 Reset" to restart the current mode

The timer will automatically switch between work and break modes when completed, and play a sound notification.

---

## 🎨 Customization

### Change Colors

Edit `src/App.css` to customize the gradient backgrounds:

```css
.app.work {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.app.break {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}
```

### Change Timer Defaults

Edit initial state values in `src/App.tsx`:

```typescript
const [workDuration, setWorkDuration] = useState<number>(25); // minutes
const [breakDuration, setBreakDuration] = useState<number>(5); // minutes
```

### Change Window Size

Edit `public/electron.js`:

```javascript
mainWindow = new BrowserWindow({
  width: 400,
  height: 400,
  // ... other options
});
```

---

## 📋 Available Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Run React app in browser |
| `npm run build` | Build React app for production |
| `npm run electron` | Run Electron app (after building React) |
| `npm run electron-dev` | Run in development mode with hot-reload |
| `npm run electron-build` | Build Electron app for all platforms |
| `npm run dist` | Build Windows installer and portable app |

---

## 🐛 Troubleshooting

### "Cannot find module 'electron-is-dev'"

Install the missing package:
```bash
npm install electron-is-dev
```

### Build fails on Windows

Make sure you have Windows Build Tools:
```bash
npm install --global windows-build-tools
```

### Audio doesn't play

The app uses an online audio file. Make sure you have an internet connection when the timer completes.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Built with [React](https://reactjs.org/)
- Powered by [Electron](https://www.electronjs.org/)
- Icons from emoji unicode
- Sound effect from [Mixkit](https://mixkit.co/)

---

## 📧 Contact

**Your Name**
- Email: your.email@example.com
- GitHub: [@yourusername](https://github.com/yourusername)

---

## 🌟 Show Your Support

Give a ⭐️ if this project helped you!

---

ib: lovesulei
Made with ❤️ and ☕
