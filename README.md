 README.md

`markdown

🎬 TikTok Comment Generator

This is a web-based app that lets users upload short videos and instantly receive AI-generated TikTok-style comments designed to engage viewers. It uses OpenAI for comment generation and Whisper for speech-to-text transcription.

---

✨ Features

- 🎥 Video Upload — Drag-and-drop or select a video file directly in the browser.
- 🧠 AI Transcription — Uses Whisper to transcribe spoken content from the video.
- 💬 Comment Generation — Generates 3 unique TikTok-style comments using OpenAI's GPT model.
- 🎭 Tone Selector — Choose from Funny, Motivational, Savage, or Friendly comment styles.
- 📋 One-Click Copy — Instantly copy any comment to paste into TikTok.
- 📱 Mobile-Friendly UI — Responsive design works smoothly on phones and tablets.
- ⚙️ Server-Side Processing — All transcription and comment generation happens securely on the backend.

---

🚀 Live Demo

Once deployed, your app will be available at:

`
https://tiktok-comment-app.onrender.com
`

---

🛠 Tech Stack

| Layer       | Tool/Library         |
|-------------|----------------------|
| Frontend    | HTML, CSS, JavaScript |
| Backend     | Flask (Python)        |
| AI Services | OpenAI GPT + Whisper  |
| Hosting     | Render                |

---

📦 Project Structure

`
tiktok-comment-app/
├── app.py             # Flask backend
├── index.html         # Frontend UI
├── requirements.txt   # Python dependencies
├── apt.txt            # System packages (ffmpeg)
├── render.yaml        # Render deployment config
└── README.md          # Project documentation
`

---

🧪 Local Development

1. Install dependencies
`bash
pip install -r requirements.txt
`

2. Set your OpenAI API key
`bash
export OPENAIAPIKEY=yourkeyhere   # Mac/Linux
set OPENAIAPIKEY=yourkeyhere      # Windows
`

3. Run the app
`bash
python app.py
`

Then open http://localhost:5000 in your browser.

---

🌐 Deploying to Render

1. Push your code to GitHub

`bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/your-username/tiktok-comment-app.git
git push -u origin main
`

2. Create a Web Service on Render

- Runtime: Python
- Build Command: pip install -r requirements.txt
- Start Command: gunicorn app:app
- Add environment variable: OPENAIAPIKEY

Render will automatically install ffmpeg via apt.txt and configure your service using render.yaml.

---

🩺 Health Check Endpoint

Render can monitor your app using:

`
/health
`

Add this to app.py:

`python
@app.route("/health")
def health():
    return "OK", 200
`

---

📄 License

This project is open-source and free to use. Attribution appreciated.

---

🙋‍♂️ Author

Built by Federick with help from Microsoft Copilot 🤝  
`

---
