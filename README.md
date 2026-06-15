<p align="center">
  <img src="public/images/logo.png" width="220" alt="NaivedyaYatra Logo" />
</p>

<h1 align="center">🪔 NaivedyaYatra 🌾</h1>
<p align="center">
  <strong>An Immersive, AI-Powered Culinary Ecosystem Preserving Ancient Indian Temple Foods & Ayurvedic Wisdom</strong>
</p>

<p align="center">
  <a href="https://6a302e95746430cba65e5f7a--capable-cucurucho-2732cc.netlify.app/"><img src="https://img.shields.io/badge/Live_Website-Deploy_on_Netlify-success?style=for-the-badge&logo=netlify&logoColor=white&color=00AD9F" alt="Live Website" /></a>
  <a href="https://github.com/AlokXCreate"><img src="https://img.shields.io/badge/GitHub-AlokXCreate-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Profile" /></a>
  <a href="https://www.linkedin.com/in/alokkadam-ai/"><img src="https://img.shields.io/badge/LinkedIn-Alok%20Kadam-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Profile" /></a>
</p>

---

## 📖 Overview

**NaivedyaYatra** is a premium, interactive web application designed to document, filter, and adapt **52 authentic, traditional Indian recipes** spanning temple offering bhogs (Prasad), regional fasting practices (Upvas/Vrat), and ancestral food preparations. 

The site utilizes a premium **modern-traditional Indian design system**—featuring deep spiritual maroon backgrounds (`#4A0E17`), warm sandalwood canvas cards, and glowing marigold gold (`#E5A93C`) interactive components. It is fully responsive and supports dynamic translation cross-fades across **8 major Indian languages** (English, Hindi, Marathi, Bengali, Tamil, Telugu, Gujarati, and Kannada).

---

## 🏗️ Detailed Architecture & System Flows

### 1. Unified System Topology

The diagram below outlines the overall layout of the application, showing how the UI views trigger the controller logic, which coordinates IndexedDB database storage, media APIs, and third-party AI models.

```mermaid
graph TB
    %% Views Layer
    subgraph Views [Client Pages & Views]
        V_Hero[Hero Page & Scroll Showcase]
        V_Lib[Recipe Library & Filters]
        V_Guru[AI Guru Workspace & Chat History]
        V_Kit[My Holy Kitchen Collections]
        V_Com[Community Hub & Review Stream]
    end

    %% Routing & Controller Layer
    subgraph Controller [Application Core]
        R_Router[State Router]
        C_App[App Controller]
        C_Translator[I18n Translation Engine]
    end

    %% Data & Models Layer
    subgraph Data [Storage & Schema Model]
        DB_Core[(IndexedDB Database Core)]
        R_Recipes[Recipe Repo - 52 Seeded Items]
        R_Users[User Auth Repo]
        R_Reviews[Reviews & base64 image Store]
        R_UserRec[Saved Collections Repo]
    end

    %% Web APIs Layer
    subgraph MediaAPIs [Browser Web Media APIs]
        A_Speech[Web Speech API: Mic & TTS]
        A_Audio[Web Audio API: Oscillator Tibetan Chime]
        A_Motion[Webcam Gesture Pixel-Shift Tracker]
    end

    %% External services
    subgraph AIEndpoints [External AI Reasoning Engines]
        E_Gemini[Google Gemini 1.5 Flash API]
        E_OpenAI[OpenAI GPT-4o Mini API]
    end

    %% Connections
    Views --> |Hash Nav Triggers| R_Router
    R_Router --> C_App
    C_Translator --> |Dynamic Cross-Fades| Views
    C_App --> |Queries & Seeding| DB_Core
    DB_Core --> R_Recipes
    DB_Core --> R_Users
    DB_Core --> R_Reviews
    DB_Core --> R_UserRec

    C_App --> |Motion Coordinates| A_Motion
    C_App --> |Synthesize Tibetan Chime| A_Audio
    C_App --> |Voice Commands| A_Speech
    C_App --> |vision payload & prompts| AIEndpoints
