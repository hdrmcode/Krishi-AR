

# 🌱 Krishi-AR

**AI-Powered Plant Disease Detection with Augmented Reality**

---

## 📌 Overview

**Krishi-AR** is an Android-based Augmented Reality application that helps farmers and agricultural workers detect plant diseases in real-time, visualize results in AR, and get expert advice through an AI chatbot — all from a smartphone.

The app combines **Machine Learning**, **Augmented Reality**, and **AI Chatbot systems** into a single unified solution.

---

## 🚀 Features

### 🔍 Real-Time Disease Detection

* Uses an ONNX-based ML model
* Runs fully **on-device (offline)**
* Detects **15 plant disease classes** (Pepper, Potato, Tomato)

### 🌿 Augmented Reality Visualization

* Displays a **3D plant model in AR**
* Anchored to real-world surfaces using ground plane detection
* Provides intuitive understanding of plant health

### 💬 AI Chatbot (AgriBotAI)

* Powered by Llama 3.3 70B via Groq API
* Answers queries about:

  * Symptoms
  * Causes
  * Treatments
* Conversational and user-friendly

### 📊 Information Panel

* Displays:

  * Disease name
  * Confidence score
  * Treatment suggestions

---

## 🛠️ Tech Stack

| Component    | Technology               |
| ------------ | ------------------------ |
| Game Engine  | Unity 2022.3 LTS         |
| AR Framework | Vuforia Engine           |
| ML Inference | Unity Sentis             |
| Model Format | ONNX                     |
| Chatbot      | Groq API (Llama 3.3 70B) |
| UI           | TextMeshPro              |
| Platform     | Android (IL2CPP, ARM64)  |

---

## 📱 Application Architecture

The project is divided into **4 core systems**:

### 1. Plant Detection (`PlantDetector.cs`)

* Captures camera region
* Preprocesses image (224×224 tensor)
* Runs ML inference using Sentis
* Outputs disease prediction

### 2. AR Visualization (`ARPlantVisualizer.cs`)

* Detects ground plane
* Places 3D plant model
* Maintains stable positioning

### 3. Information Panel (`PlantInfoPanel.cs`)

* Displays diagnosis details
* Color-coded:

  * 🟢 Healthy
  * 🔴 Diseased

### 4. AI Chatbot (`PlantChatbot.cs`)

* Sends queries to Groq API
* Displays conversational responses
* Handles errors (API key, rate limits, etc.)

---

## ⚙️ Installation & Setup

### 🔧 Requirements

* Unity 2022.3 LTS
* Android Build Support (SDK, NDK)
* Vuforia Engine
* Unity Sentis Package

### 📥 Steps

1. Clone the repository

```bash
git clone https://github.com/your-username/krishi-ar.git
```

2. Open project in Unity

3. Add your Groq API key

```
Assets/Resources/groq_key.txt
```

4. Build for Android

* Platform: Android
* Architecture: ARM64
* Backend: IL2CPP

5. Install APK on device

---

## 📊 Results

* ✅ Smooth real-time detection (no lag using async inference)
* ✅ Accurate classification under good lighting
* ✅ Stable AR placement within 2–5 seconds
* ✅ Chatbot responses in ~2–4 seconds

---

## ⚠️ Limitations

* ❌ Accuracy drops in low lighting or motion blur
* ❌ Chatbot requires internet connection
* ❌ AR struggles on reflective or textureless surfaces

---

## 🔮 Future Improvements

* 🌾 Support more crops (Rice, Wheat, Cotton, etc.)
* 📡 Offline chatbot using on-device LLM
* 🎥 Continuous detection (no capture button)
* 📈 Disease severity estimation
* 🌐 Multilingual support (Hindi, Kannada, Tamil, etc.)
* 🧾 Detection history & analytics
* ☁️ Cloud dashboard for outbreak tracking

---

## 🎯 Use Case

* Farmers in rural areas
* Agricultural students
* Field researchers
* Smart farming applications

---

## 📚 References

* PlantVillage Dataset
* Unity Sentis Documentation
* Vuforia Engine Docs
* Groq API (Llama 3)
* FAO Agricultural Reports

---

## 👨‍💻 Author

**Hariduthram PS**
B.Tech Information Technology (AR/VR)


---

## 📄 License

This project is for academic and research purposes.

