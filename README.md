***

```markdown
# 🚀 ResumeMatch V4: AI-Powered Career Coach & Builder

![Kotlin](https://img.shields.io/badge/Kotlin-B125EA?style=for-the-badge&logo=kotlin&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?style=for-the-badge&logo=android&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Gemini AI](https://img.shields.io/badge/Google_Gemini-8E75B2?style=for-the-badge&logo=google&logoColor=white)

**ResumeMatch V4** is a flagship Android application designed to be an end-to-end AI career platform. It combines a dynamic Jetpack Compose frontend with a lightning-fast Python FastAPI backend to deliver real-time ATS analysis, on-the-fly PDF resume generation, and a fully interactive, 3D real-time AI Voice Interview Coach.

---

## ✨ Signature Features

### 🎙️ Live 3D AI Voice Coach
* **Real-Time Voice Interviews:** Engage in live, timed mock interviews with an AI trained to act as a Senior Technical Recruiter.
* **Dynamic 3D UI:** Features a custom-built, trigonometric 3D point-cloud sphere that fluidly reacts to speaking, listening, and processing states—all drawn natively on a Jetpack Compose Canvas.
* **Recruiter Scorecard:** Upon concluding the interview, the AI generates a brutally honest, comprehensive feedback report grading your communication, technical accuracy, and overall hireability.

### 📄 Intelligent Resume & JD Analysis
* **ATS Scoring Engine:** Upload your PDF resume and paste a Job Description. The Gemini 2.5 Flash model processes the text to calculate a realistic ATS match score.
* **Skill Gap Analysis:** Automatically identifies top matched skills and critical missing skills, offering actionable bullet-point suggestions to improve your resume.

### 🛠️ Generative PDF Builder
* **Dynamic PDF Rendering:** The Python backend utilizes `ReportLab` to programmatically render perfectly formatted PDF resumes in milliseconds.
* **Multiple Templates:** Supports both ultra-clean ATS-compliant templates and visually striking Modern templates with profile picture support.

### 🧠 AI Master Vault & Cloud Sync
* **Conversational Data Entry:** Chat with the AI Assistant to naturally extract your experience, projects, and skills. The AI parses the conversation and structures your data into JSON.
* **Supabase Integration:** Securely syncs your Master Vault to the cloud using Supabase, ensuring your profile is never lost.

---

## 🏗️ System Architecture

The project is split into two distinct codebases communicating via a RESTful architecture:

1. **The Client (Android):** Built entirely in Kotlin using Jetpack Compose, Coroutines, and OkHttp. It handles all UI rendering, Speech-to-Text (STT), Text-to-Speech (TTS), and local device states.
2. **The Server (Python/FastAPI):** A stateless backend hosted on Render. It handles the heavy lifting: communicating with the Google Gemini API, parsing PDFs via `pypdf`, structuring JSON outputs, and drawing generative PDFs.

---

## 🚀 Installation & Setup

### 1. Backend Setup (FastAPI)
1. Clone the backend repository.
2. Install the required Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Create a `.env` file in the root directory and add your Google Gemini API Key:
   ```env
   GEMINI_API_KEY=your_gemini_api_key_here
   ```
4. Run the server locally:
   ```bash
   uvicorn main:app --reload
   ```

### 2. Android App Setup
1. Clone the Android repository and open it in **Android Studio** (Requires Android SDK 36).
2. To secure your Supabase credentials, open the `local.properties` file in the root of the Android project and add:
   ```properties
   SUPABASE_URL="[https://your-project-id.supabase.co](https://your-project-id.supabase.co)"
   SUPABASE_KEY="your-anon-public-key"
   ```
3. Sync the project with Gradle files. The `BuildConfig` will automatically inject these keys safely into the app.
4. Update the `apiBaseUrl` variable in the UI to point to your hosted Render backend (or your local IP if testing locally).
5. Build and Run the APK!

---

## 📸 Showcase
<img width="540" height="1107" alt="RMV3-1" src="https://github.com/user-attachments/assets/3a39bf56-0194-403a-aa6d-f37f8ffe43f9" />
<img width="540" height="1107" alt="RMV3-2" src="https://github.com/user-attachments/assets/4947feb0-9770-428d-8df0-55f975d44e57" />
<img width="540" height="1107" alt="RMV3-3" src="https://github.com/user-attachments/assets/89edbeb1-f4b3-4993-bbd6-cb62f5ec3d7f" />
<img width="540" height="1107" alt="RMV3-4" src="https://github.com/user-attachments/assets/f660047a-8797-441f-ad68-26266dfbcf01" />
<img width="540" height="1107" alt="RMV3-5" src="https://github.com/user-attachments/assets/6b5fdeaf-e0fe-4845-afa7-9fbb79e29b61" />


---

## 🛡️ Privacy & Security
* **No Hardcoded Keys:** All API keys are strictly managed via environment variables (`.env`) and Android's `local.properties` to ensure zero credential leakage.
* **Stateless AI:** The backend does not store resume data; it processes requests in memory and immediately returns the result to the client.

---
*Designed and engineered by Rehan.*
```
