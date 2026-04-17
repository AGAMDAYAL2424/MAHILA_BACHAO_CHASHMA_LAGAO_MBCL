# MBCL (Mahila Bachao Chashma Lagao) 👓
**Project Information & Technical Overview**

---

## 1. Executive Summary
**MBCL (Mahila Bachao Chashma Lagao)** aims to create a fear-free world for women by strengthening law and order through technology. The project proposes state-of-the-art, AI-powered safety smart glasses designed to be discreet, highly functional, and unbelievably affordable. 

### The Problem
According to UNICEF and WHO data:
* Roughly 1 in 8 girls and women globally (370 million) have experienced rape or sexual assault before turning 18.
* 1 in 3 women (approx. 736 million) have faced physical or sexual violence in their lifetime.
* 6% of women globally specifically report sexual assault by a non-partner.

### The Solution
A pair of safety smart glasses priced at just **$20–$30** and weighing only **40–50 grams**. They are designed with magnetic clip-on frames (allowing for powered, blue-cut, or sunglass lenses) so they blend in perfectly as standard everyday eyewear.

---

## 2. Hardware Architecture
The glasses are packed with edge-computing hardware to ensure rapid response and reliable evidence collection:

* **Microcontroller:** Xiao ESP32S3 
* **Vision:** Front-facing HD Camera
* **Audio:** High-sensitivity noise-cancelling microphone (INMP441) and HD Speaker
* **Location:** GP02 GNSS for real-time tracking
* **Connectivity:** EC200G Nano 4G LTE Module for direct-to-cloud streaming
* **Power:** Integrated stealth battery
* **Controls:** Touch sensors and physical buttons

---

## 3. Software & AI Capabilities
MBCL leverages a robust mix of edge computing and cloud AI to protect users in real-time. The core tech stack includes **Azure, Swift, Python, Node.js, C++, and TensorFlow Lite**.

### AI Threat Detection & Activation
* **Voice Recognition (Azure Speech Services):** The glasses constantly process audio locally. Upon hearing a specific, user-defined wake-word, the system activates.
* **Facial Recognition (Azure Face API & OpenCV):** The camera actively scans faces and cross-references them with the NCRB (National Crime Records Bureau) database of known sexual offenders. If a match is found, the user receives an immediate alert on their phone.
* **Edge Computing:** Utilizes AWS Greengrass or OpenHorizon for localized processing, paired with TensorFlow Lite models trained specifically for ESP-32.

### Secure Evidence Workflow
1. **Trigger:** Activated via physical button, gesture, app, or voice wake-word.
2. **Recording:** Captures video (.avi converted to .mp4 via a virtual function) and audio.
3. **Data Protection:** Uses AES-256 encryption to protect data from cyber attacks.
4. **Cloud Storage:** Streams directly via the 4G LTE module using short-term 'Write' SAS tokens to an **Immutable Azure Blob Storage**, ensuring the evidence cannot be tampered with or deleted, even if the glasses are destroyed.

---

## 4. Mobile Application
The MBCL companion app provides a central hub for safety management and device control:
* **Live GPS Tracking:** View the user's location, nearest police stations, and home base on an integrated map. 
* **Location Sharing:** Toggle live location sharing with pre-set favorite contacts.
* **Emergency Settings:** Set custom keywords for "ON" and "OFF" alert modes (e.g., setting a specific SOS word). 
* **Media Management:** Securely view and playback recorded audio and video files synced from the glasses.
* **Emergency Features:** Includes a "4 Taps Emergency Mode" and an SOS dialer with immediate access to 112, muted calls, and quick-contact notification.

---

## 5. Feasibility & Impact
* **Social Impact:** Creates a safer environment for women while instilling fear among criminals.
* **Judicial Impact:** Facilitates fast reporting and provides immutable video/audio evidence, increasing successful crime reporting.
* **Economic Feasibility:** High potential for international funding and government grants.
* **Technical Feasibility:** Highly affordable and self-sustainable architecture.

---

## 6. Go-To-Market Strategy
The project targets the intersection of the Eyewear Market ($6.18 Billion, projected 100% growth by 2030) and the Women's Safety Products Market ($1.9 Billion, projected 150% increase). 

**Business Model:**
* **Retailing:** Selling the base MBCL frame, plain lenses, and charging box.
* **Replacements & Add-ons:** Selling different styles of magnetic clip-ons, powered lenses, and replacement batteries.
* **Subscriptions:** Optional yearly or quarterly plans for software upgradations, premium cloud storage, and battery replacements.
* **Distribution:** OEM "No Brand" partnerships, direct advertisement, social media, and government safety campaigns.

---

## 7. Competitive Analysis
MBCL disrupts the current smart glasses market by offering crucial safety features at a fraction of the cost of lifestyle smart glasses.

| Features | MBCL | RayNeo-X2 | RayBan-Meta | Lenskart Phonic | Titan EyeX |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Price** | **$20 - $30** | $750 | $300 | $55 | $200 |
| **Camera Recording** | ✅ | ✅ | ✅ | ❌ | ❌ |
| **Integrated GPS Module**| ✅ | ❌ | ❌ | ❌ | ❌ |
| **Dedicated Calling** | ✅ | ❌ | ❌ | ❌ | ❌ |
| **Microphone** | ✅ | ✅ | ✅ | ✅ | ✅ |
