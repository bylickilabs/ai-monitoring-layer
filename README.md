# 🧠 BYLICKILABS – AI Monitoring Layer  
**Version 1.0.0 — Client-Side Analytics & Intelligent Anomaly Detection**

The **AI Monitoring Layer** is a fully client-side monitoring, diagnostics, and anomaly-scoring engine designed for modern web applications.  
It captures performance signals, network failures, runtime errors, FPS degradation, offline events, and generates structured incident reports — including optional screenshot export (via html2canvas).

## 🚀 Key Features
- **Real-time JavaScript error tracking**
- **Network monitoring** (fetch + XHR interception)
- **Resource load failure detection**
- **FPS & rendering performance analysis**
- **AI Scoring 2.0** (event-based anomaly evaluation)
- **Offline event awareness**
- **Incident Report Generator** (JSON export)
- **Screenshot Capture** *(optional – requires html2canvas)*
- **Built-in UI Monitoring Overlay** (status, logs, tools)

## 📦 Installation via npm
```
npm install @bylickilabs/ai-monitoring-layer
```

Import inside your project:
```js
import "@bylickilabs/ai-monitoring-layer";
```

## 🌐 CDN
```
https://cdn.jsdelivr.net/npm/@bylickilabs/ai-monitoring-layer/ai.min.js
https://unpkg.com/@bylickilabs/ai-monitoring-layer/ai.min.js
```

---

## 🌐 CDN Integration

### Primary + Fallback CDN Setup
```html
<script src="https://cdn.jsdelivr.net/npm/@bylickilabs/ai-monitoring-layer/ai.min.js" defer></script>

<script 
    defer
    onerror="loadFallback()"
    src="https://unpkg.com/@bylickilabs/ai-monitoring-layer/ai.min.js">
</script>

<script>
function loadFallback() {
    if (!window.BYLICKILABS_AI_MONITOR) {
        const s = document.createElement('script');
        s.src = 'ai.min.js';
        document.head.appendChild(s);
    }
}
</script>
```

## 🔧 Local Integration
```html
<script src="ai.min.js" defer></script>
```

---

## 📘 Usage
```js
window.BYLICKILABS_AI_MONITOR.init();
BYLICKILABS_AI_MONITOR.exportLogs();
BYLICKILABS_AI_MONITOR.exportIncidentReport();
BYLICKILABS_AI_MONITOR.captureScreenshot();
BYLICKILABS_AI_MONITOR.logCustom("info", "Custom event triggered");
```

## 🛡 License
[LICENSE](LICENSE)
