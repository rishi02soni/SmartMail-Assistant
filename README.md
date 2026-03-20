# SmartMail-Assistant
SmartMail Assistant 🤖✉️

SmartMail Assistant is a powerful AI-powered Chrome extension that helps you draft and reply to emails instantly, directly within your inbox. Built with a modern full-stack architecture, it boosts productivity and streamlines email communication.

<!-- Add a screenshot or GIF later -->


✨ Features

⚡ Instant Reply Generation: Generate context-aware email replies in seconds using Google Gemini AI.

🎭 Tone Customization: Select from multiple tones (Professional, Casual, Friendly) to match your conversation style.

🔌 Seamless Gmail Integration: Works directly inside Gmail—no switching tabs or copy-pasting required.

📋 One-Click Copy: Copy the generated text to your clipboard with a single button.

🛡️ Secure: Your email data is processed securely via a private backend; no unnecessary storage.

🛠️ Tech Stack
Frontend (Chrome Extension)

React.js

Material-UI (MUI) for a modern interface

Chrome Extensions Manifest V3

Backend (API Server)

Spring Boot & Java

WebClient for reactive HTTP requests

Spring Boot Actuator (monitoring)

AI & Cloud Services

Google Gemini API

Prompt engineering for optimized AI responses

🚀 Installation & Setup
Prerequisites

Node.js (v18 or higher)

npm or yarn

Java 17 or higher

Maven

Google Cloud Project with Gemini API enabled and an API key

1. Clone the Repository
git clone https://github.com/your-username/SmartMail-Assistant.git
cd SmartMail-Assistant

2. Backend (Spring Boot) Setup
cd backend



Create src/main/resources/application.yml:

gemini:
  api:
    key: YOUR_GEMINI_API_KEY
    url: https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent
server:
  port: 8080


Run the backend:

mvn spring-boot:run


The API server will start at http://localhost:8080.

3. Frontend (Chrome Extension) Setup
cd frontend
npm install


Update the API endpoint if needed (e.g., http://localhost:8080).

Build for production:

npm run build


Load the extension in Chrome:

Open chrome://extensions/

Enable Developer mode

Click Load unpacked

Select the build or dist folder

4. Using the Extension

Pin SmartMail Assistant to your toolbar

Open Gmail and select an email

Click the extension icon

Select your desired tone and click Generate Reply

Copy the generated text to Gmail and send

📁 Project Structure
SmartMail-Assistant/
├── backend/                  # Spring Boot Application
│   ├── src/main/java/com/em/EmailWriter/
│   │   ├── Controller/       # REST API endpoints
│   │   ├── Services/         # Business logic
│   │   ├── Model/            # Data objects
│   │   └── Application.java
│   └── pom.xml
└── frontend/                 # Chrome Extension (React)
    ├── public/               # Manifest, icons, HTML
    ├── src/
    │   ├── components/       # React components (App.js)
    │   └── ...
    ├── package.json
    └── manifest.json

🔌 API Reference

Generate a Reply
POST /api/email/generate

Request Body:

{
  "emailContent": "The full text of the email to reply to...",
  "tone": "Professional" // Optional: "Professional", "Casual", "Friendly"
}


Success Response:

Code: 200 OK
Content: "The generated email reply text."

🤝 Contributing

Contributions, issues, and feature requests are welcome!

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request


🙋‍♂️ Author

Rishi Soni

GitHub:https://github.com/rishi02soni/
