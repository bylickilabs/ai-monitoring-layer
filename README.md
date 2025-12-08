# 🧠 BYLICKILABS – AI Monitoring Layer  
**Version 1.1.0 — Client-Side Analytics & Intelligent Anomaly Detection**

| [LIVE DEMO](https://github.com/bylickilabs/EncryptStudio-Website) |
|---|

| <img width="1280" height="640" alt="ai layer" src="https://github.com/user-attachments/assets/572c80f1-21a8-4459-be2f-6fea63a272da" /> |
|---|

> The **AI Monitoring Layer** is a fully client-side monitoring, diagnostics, and anomaly-scoring engine designed for modern web applications.  
  - It captures performance signals, network failures, runtime errors, FPS degradation, offline events, and generates structured incident reports — including optional screenshot export (via html2canvas).

<br>

---

<br>

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

<br>

---

<br>

## 🌐 CDN
```
<script src="https://cdn.jsdelivr.net/npm/@bylickilabs/ai-monitoring-layer/ai.min.js" defer></script>
<script src="https://unpkg.com/@bylickilabs/ai-monitoring-layer/ai.min.js" defer></script>
```

> Dependencies

```
<script src="https://cdn.jsdelivr.net/npm/html2canvas@1.4.1/dist/html2canvas.min.js"></script>
```

<br>

---

<br>

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

<script>
if ("serviceWorker" in navigator) {
    window.addEventListener("load", () => {
        navigator.serviceWorker.register("/service-worker.js")
            .then(reg => {
                console.log("PWA Service Worker activated:", reg.scope);
            })
            .catch(err => {
                console.error("PWA Service Worker error:", err);
            });
    });
}
</script>
```
<br>

---

<br>

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
