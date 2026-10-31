# EduMate+ Web - Offline AI Learning Assistant

A Progressive Web App (PWA) that provides five AI-powered learning modules completely offline, designed specifically for dyslexia support and accessibility.

## 🚀 Features

### AI Modules (100% Offline)
- **📸 OCR Scanner**: Camera-based text recognition with Tesseract.js
- **📝 Text Simplifier**: NLP-powered content simplification for different reading levels
- **🔊 Text-to-Speech**: Customizable voice synthesis with Web Speech API
- **😊 Emotion Detection**: Real-time facial expression analysis for adaptive learning
- **✋ Gesture Control**: Hands-free navigation with MediaPipe gesture recognition

### Accessibility First
- **Dyslexia-friendly fonts** (Lexend, OpenDyslexic)
- **High contrast themes** and color vision support
- **Emotion-aware UI** that adapts to stress/frustration
- **Large touch targets** (44px minimum)
- **Screen reader optimized** with ARIA labels
- **Keyboard navigation** throughout

### Privacy & Offline
- **Zero telemetry** - no data collection
- **Complete offline functionality** - all AI runs in browser
- **Local storage only** - settings saved on device
- **No external API calls** after initial load

## 🛠️ Technology Stack

- **Frontend**: React 18 + TypeScript + Vite
- **Styling**: Tailwind CSS + Custom Design System
- **AI/ML**: TensorFlow.js, Tesseract.js, MediaPipe, Web Speech API
- **PWA**: Service Worker, App Manifest, Offline Caching
- **Accessibility**: ARIA, WCAG 2.1 AA compliant

## 🏃‍♂️ Quick Start

### Prerequisites
- Node.js 16+ and npm
- Modern browser with camera/microphone access

### Installation
```bash
# Clone repository
git clone [repository-url]
cd edumate-web

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### PWA Setup
```bash
# Build and serve locally
npm run build
npm run preview

# Install as PWA
# 1. Open in Chrome/Edge
# 2. Click install icon in address bar
# 3. App runs offline after installation
```

## 📱 Usage

### Getting Started
1. **Launch**: Open app and allow camera/microphone permissions
2. **Navigate**: Use sidebar or gesture controls to switch modules
3. **Customize**: Access settings panel for accessibility preferences
4. **Start Learning**: Begin with OCR scanner or text simplifier

### Module Workflows
```
OCR → Text Simplifier → Text-to-Speech
     ↓
Emotion Detection (monitors throughout)
     ↓
Gesture Control (hands-free navigation)
```

### Keyboard Shortcuts
- `Tab/Shift+Tab`: Navigate elements
- `Enter/Space`: Activate buttons
- `Esc`: Close modals/panels
- `Arrow keys`: Navigate lists

## 🔧 Configuration

### Accessibility Settings
```javascript
// Default settings in AccessibilityProvider
{
  fontSize: 'medium',           // small|medium|large|extra-large
  contrast: 'normal',           // normal|high
  dyslexiaFont: true,          // Enable dyslexia-friendly fonts
  reducedMotion: false,        // Reduce animations
  voiceCommands: false,        // Voice navigation
  colorBlindness: 'none'       // none|protanopia|deuteranopia|tritanopia
}
```

### AI Model Configuration
```javascript
// OCR Settings (Tesseract.js)
{
  language: 'eng',
  worker: 2,                   // Parallel workers
  tessedit_char_whitelist: '', // Character restrictions
}

// TTS Settings (Web Speech API)
{
  rate: 1.0,                   // 0.1 - 10
  pitch: 1.0,                  // 0 - 2
  volume: 1.0,                 // 0 - 1
}
```

## 🧪 Testing

### Accessibility Testing
```bash
# Install axe-core for accessibility testing
npm install @axe-core/playwright --save-dev

# Run accessibility tests
npm run test:a11y

# Manual testing checklist:
# ✅ Screen reader navigation
# ✅ Keyboard-only navigation
# ✅ Color contrast ratios
# ✅ Focus indicators
# ✅ Touch target sizes
```

### PWA Testing
```bash
# Lighthouse PWA audit
npx lighthouse http://localhost:4173 --view

# Required scores:
# Performance: >90
# Accessibility: >95
# Best Practices: >90
# SEO: >90
# PWA: >90
```

## 🚀 Deployment

### Static Hosting (Recommended)
```bash
# Build for production
npm run build

# Deploy to Vercel
npx vercel

# Deploy to Netlify
npm install -g netlify-cli
netlify deploy --prod --dir=dist
```

### Self-Hosting
```bash
# Build application
npm run build

# Serve with any static server
python -m http.server 8080 -d dist
# or
npx serve dist
```

## 🛡️ Privacy Declaration

**EduMate+ Web is completely private:**
- ✅ All AI processing happens locally in your browser
- ✅ No data is sent to external servers
- ✅ No analytics or tracking
- ✅ No cookies except for local settings
- ✅ Camera/microphone data never leaves your device
- ✅ All models downloaded once and cached offline

## 📊 Performance

### Lighthouse Scores (Target)
- **Performance**: 95+
- **Accessibility**: 98+
- **Best Practices**: 95+
- **SEO**: 90+
- **PWA**: 100

### Model Sizes (Approximate)
- Tesseract.js (OCR): ~10MB
- TensorFlow.js models: ~5MB
- MediaPipe models: ~3MB
- Total offline cache: ~20MB

## 🤝 Contributing

### Code Style
- TypeScript with strict mode
- ESLint + Prettier configuration
- Semantic component naming
- Accessibility-first development

### Adding New Features
1. Follow existing component structure
2. Add comprehensive TypeScript types
3. Include accessibility testing
4. Update documentation

## 📄 License

MIT License - see LICENSE file for details.

## 🆘 Support

### Common Issues
- **Camera not working**: Check browser permissions
- **TTS not speaking**: Ensure audio permissions granted
- **Slow performance**: Try reducing model complexity in settings
- **Gesture detection fails**: Ensure good lighting and clear background

### Browser Compatibility
- ✅ Chrome 90+ (recommended)
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

### System Requirements
- **RAM**: 4GB minimum, 8GB recommended
- **Storage**: 100MB available space
- **Camera**: Any webcam for OCR/emotion detection
- **Microphone**: For voice commands (optional)

---

Built with ❤️ for accessibility and inclusive learning.