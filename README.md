

<h1 align="center">🪔 NaivedyaYatra 🌾</h1>
<p align="center">
  <strong>An Immersive, AI-Powered Culinary Ecosystem Preserving Ancient Indian Temple Foods & Ayurvedic Wisdom</strong>
</p>

<p align="center">
  <a href="https://github.com/AlokXCreate"><img src="https://img.shields.io/badge/GitHub-AlokXCreate-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Profile" /></a>
    <a href="https://6a302e95746430cba65e5f7a--capable-cucurucho-2732cc.netlify.app/"><img src="https://img.shields.io/badge/Live_Website-Deploy_on_Netlify-success?style=for-the-badge&logo=netlify&logoColor=white&color=00AD9F" alt="Live Website" /></a>
    <a href="https://animated-zabaione-9e4cab.netlify.app/"><img src="https://img.shields.io/badge/Project Report-Naivedya%20Yatra-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Profile" /></a>
  <a href="https://www.linkedin.com/in/alokkadam-ai/"><img src="https://img.shields.io/badge/LinkedIn-Alok%20Kadam-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Profile" /></a>
</p>

---

## 📖 Overview

**NaivedyaYatra** is a premium, interactive web application designed to document, filter, and adapt **52 authentic, traditional Indian recipes** spanning temple offering bhogs (Prasad), regional fasting practices (Upvas/Vrat), and ancestral food preparations. 

The site utilizes a premium **modern-traditional Indian design system**—featuring deep spiritual maroon backgrounds (`#4A0E17`), warm sandalwood canvas cards, and glowing marigold gold (`#E5A93C`) interactive components. It is fully responsive and supports dynamic translation cross-fades across **8 major Indian languages** (English, Hindi, Marathi, Bengali, Tamil, Telugu, Gujarati, and Kannada).

---

## ✨ Core Features & Technical Highlights

### 1. 🎙️ AI Culinary Guru & Secure API Portal
* **ChatGPT-Style Sidebar**: A dual-column layout hosting a local browser-cached **Sacred Chat History** stream (grouped chronologically by *Today*, *Yesterday*, and *Previous 7 Days*) and a **Dietary Parameters** configurations panel.
* **Granular Dietary Guardrails**: The Guru automatically evaluates queries using strict traditional laws:
  * **Sattvic / Jain**: Omit root vegetables (onions/garlic) and substitute potatoes with Raw Banana (*Kacha Kela*).
  * **Upvas / Vrat (Fasting)**: Automatically filters out regular grains, replacing table salt with Sendha Namak (Rock Salt) and standard flours with water chestnut/arrowroot flour.
* **Secure API Portal**: A glassmorphic connection modal with secure local key storage for Google Gemini, OpenAI, and Anthropic Claude endpoints, featuring connection diagnostics and visual eye toggles.
* **Multimedia Inputs**: Supports uploading images for recipe analysis (Base64 visión encoding), text file attachments, and real-time voice microphone transcription.

### 2. 🍳 Interactive 'Rasoi' Cooking Mode
* **Splash-Resistant parchment Overlay**: A fullscreen, distraction-free interface with enlarged typography tailored for active kitchen environments.
* **Non-Linear 'Festival Scale Multiplier'**: Scales recipe portions accurately from **1 up to 50 servings** using food-science batch curves:
  * *Potent Spices & Herbs* scale sub-linearly (`multiplier^0.72`) to keep flavors balanced.
  * *Trace items* (Salt, Camphor, Baking Soda) scale sub-linearly (`multiplier^0.55`) to avoid chemical/over-salting issues.
  * *Liquids & Water* scale sub-linearly (`multiplier^0.85`) due to lower relative evaporation in large vessels.
  * *Main Grains, Flour & Ghee* scale linearly (`multiplier^1.0`).
* **Hands-Free Webcam Gesture Controls**: Track hand waves using a lightweight pixel brightness shifting algorithm, allowing you to advance instructions without touching the screen with dirty fingers.
* **Localized Vocal Navigation**: Voice command triggers in all 8 languages:
  * *"Guru Next"* / *"आगे"* / *"पुढचे"* -> Advance step.
  * *"Guru Back"* / *"पीछे"* / *"मागे"* -> Previous step.
  * *"Guru Repeat"* / *"फिर से"* / *"पुन्हा"* -> Vocalizes active instructions via Text-to-Speech synthesis.
* **Tibetan Singing Bowl Chime**: Uses Web Audio API oscillators to synthesize a resonant Tibetan bowl chime (harmonic frequencies: `220Hz`, `440Hz`, `560Hz`, `680Hz`, `880Hz` with a `5s` decay) when timers expire.

### 3. 🍃 Offline Recipe Library & Search
* **52 Aligned Seeding Records**: Contains comprehensive, authenticated descriptions, prep/cook times, elder tips, and community reviews.
* **High-Fidelity Food Photography**: Features 22 custom-generated, photorealistic culinary assets tailored specifically for each unique dish.
* **Phonetic Synonyms Search**: Search index matching spelling variations (e.g. searching `potato` or `batata` correctly matches potatoes; `curd` or `doi` matches yogurt-based meals).

---

## 🛠️ Architecture & Tech Stack

```mermaid
graph TD
    UI[HTML5 / Vanilla CSS3 / Sandalwood Canvas UI] --> |Route Handlers| Router[State Router]
    Router --> App[App Controller]
    App --> |IndexedDB Transactions| DB[(IndexedDB Store)]
    App --> |Web Speech API| Vocal[Vocal Commands & TTS]
    App --> |Web Audio API| Audio[Singing Bowl Synthesizer]
    App --> |Canvas Frame Capture| Motion[Webcam Motion Detector]
    App --> |Rest HTTPS Fetch| API[OpenAI / Gemini / Claude API]
