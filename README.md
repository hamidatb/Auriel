# 🌟 Auriel - Your AI Productivity Companion 🌟

**Auriel** is an AI-powered productivity assistant I created to serve as a second brain. Designed for iOS, Auriel helps you manage your classes, organize tasks, capture ideas, and streamline your daily workflow with intelligent reminders and personalized assistance. Currently in the early stages of development, Auriel aims to enhance your productivity by taking care of the details so you can focus on what truly matters. 🚀

---

## 📋 Table of Contents

1. [About Auriel](#about-auriel)
2. [🌟 Summary](#-summary)
3. [🚀 Features](#-features)
4. [🛠 Getting Started](#-getting-started)
5. [📂 Project Structure](#-project-structure)
6. [🧰 Tech Stack](#-tech-stack)
7. [📡 APIs & Integrations](#apis--integrations)
8. [📝 Contributing](#-contributing)
9. [📜 License](#-license)
10. [📢 Feedback & Support](#-feedback--support)

---

## About Auriel

**Auriel** is my personal AI-driven assistant designed to function as a second brain. By integrating with tools like Google Calendar and Gmail, Auriel helps you stay organized, manage your tasks efficiently, and keep track of your ideas effortlessly. Whether you're a student juggling multiple classes or a professional handling numerous projects, Auriel is here to streamline your productivity.

---

## 🌟 Summary

I'm developing **Auriel** as a comprehensive AI assistant to enhance personal productivity. Leveraging SwiftUI for the frontend and Firebase for the backend, Auriel integrates seamlessly with Google services and utilizes OpenAI's GPT-4 for intelligent task management and email assistance. As the sole developer, I'm committed to building a user-friendly and efficient tool that acts as your digital second brain, helping you stay organized and focused.

---

## 🚀 Features

### 🌅 Phase 1 - Minimum Viable Product (MVP)
Core functionality to help you get started with Auriel:

- **🗓 Class Management**: Integrates with Google Calendar to track your classes.
- **🔔 Task Reminders**: Sends reminders after each class to add related tasks.
- **📅 Daily Rundown**: Morning and evening summaries to keep your day organized.
- **💡 Idea Management**: Quick-entry for spontaneous ideas, with reminders to follow up.
- **🎨 Customizable Settings**: Set your preferred interaction style and notification options.

### 🌱 Future Enhancements (Phase 2 & 3)
Features to deepen Auriel’s utility:

- **📬 Email and Messaging Assistant**: AI-driven email drafts with context.
- **🍽 Meal Planning**: Personalized meal suggestions based on what’s in your fridge.
- **💼 Career Opportunity Finder**: Summaries of relevant scholarships, internships, and conferences.


---

## 🛠 Getting Started

### Prerequisites

- **Xcode 13+** with SwiftUI support
- **Firebase Account** for Authentication and Firestore
- **Google API Credentials** for accessing Google Calendar and Gmail

### Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/Auriel.git
   cd Auriel
   ```

2. **Firebase Setup**

   - Create a Firebase project and enable **Firestore** and **Authentication**.
   - Download the `GoogleService-Info.plist` file from Firebase and add it to the `AurielXcode/` directory in Xcode.

3. **Google API Setup**

   - Enable **Google Calendar** and **Gmail API** in the [Google Cloud Console](https://console.cloud.google.com/).
   - Set up OAuth 2.0 credentials and download the credentials file.
   - Place the credentials in `backend/functions/` and configure `calendar.js` and `email.js`.

4. **Install Firebase CLI**

   ```bash
   npm install -g firebase-tools
   firebase login
   firebase init
   ```

   - Select **Functions** during setup and add Firebase config to `backend/firebase.json`.

5. **Install Backend Dependencies**

   ```bash
   cd backend/functions
   npm install
   ```

6. **Deploy Firebase Functions**

   ```bash
   firebase deploy --only functions
   ```

7. **Run the iOS App**

   - Open `AurielXcode/Auriel.xcodeproj` in Xcode.
   - Select a simulator or physical device and click **Run**.

---

## 📂 Project Structure

```plaintext
Auriel/
├── AurielXcode/                 # iOS App Code
│   ├── Auriel.xcodeproj/        # Xcode project files
│   ├── Assets/                  # Images, icons, colors, etc.
│   ├── Models/                  # Data models (e.g., User.swift, Task.swift, Idea.swift)
│   ├── Views/                   # UI Views (Main Dashboard, Task Entry Screen, etc.)
│   ├── ViewModels/              # MVVM ViewModels for state management
│   ├── Services/                # API handlers (e.g., Google Calendar, Gmail, Notifications)
│   ├── Utils/                   # Utility functions and constants
│   └── App.swift                # Main application entry point
│
├── backend/                     # Backend Code (Firebase Cloud Functions)
│   ├── functions/               # Cloud functions
│   │   ├── index.js             # Main entry point for Firebase Functions
│   │   ├── api/                 # API-specific handlers
│   │   │   ├── calendar.js      # Google Calendar integration
│   │   │   ├── email.js         # Gmail API handling
│   │   │   ├── notifications.js # Notifications and reminders
│   ├── firebase.json            # Firebase configuration file
│   └── package.json             # Node.js dependencies for Firebase Functions
│
├── docs/                        # Documentation and assets
│   ├── api_documentation.md     # API documentation and endpoints
│   ├── design/                  # Figma exports, mockups, screenshots
│   ├── user_personas.md         # Descriptions of target user personas and use cases
│   └── roadmap.md               # Development roadmap and milestones
│
├── frontend/                    # Frontend assets (if separate from AurielXcode)
│   └── ...                      # Additional frontend resources
│
├── .gitignore                   # Git ignore file
├── README.md                    # Main README file for the project
└── LICENSE                      # Project license
```

---

## 🧰 Tech Stack

- **Frontend**: SwiftUI for iOS UI components
- **Backend**: Firebase (Firestore, Authentication, Cloud Functions)
- **APIs**: Google Calendar, Gmail, OpenAI GPT-4 for AI responses
- **Push Notifications**: Firebase Cloud Messaging (FCM)

---

## 📡 APIs & Integrations

1. **Google Calendar API**: Imports and manages class schedules.
2. **Google Tasks API**: Allows task addition and reminders.
3. **Gmail API**: Detects and drafts responses for relevant emails.
4. **OpenAI GPT-4 API**: Contextual task prompts, email responses, and reminders.

---

## 📝 Contributing

Contributions are what make the open-source community such a great place! As the sole developer, I appreciate any feedback, suggestions, or contributions to help Auriel grow. Here’s how you can help:

1. **Fork the Repository**: Click the “Fork” button at the top of this page.
2. **Create a Branch**: Use a descriptive name for your branch.

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Commit Your Changes**: Write clear, meaningful commit messages.
4. **Push Your Branch**:

   ```bash
   git push origin feature/your-feature-name
   ```

5. **Open a Pull Request**: Compare changes and submit.

Check out my [CONTRIBUTING.md](CONTRIBUTING.md) for more detailed guidelines.

---

## 📜 License

Distributed under the MIT License. See [LICENSE](LICENSE) for more information.

---

## 📢 Feedback & Support

If you have any questions, suggestions, or just want to say hi, feel free to open an issue or reach out to me directly. Auriel is an evolving project, and your insights are invaluable to making it a truly helpful “second brain” for productivity! ❤️

---

Thank you for checking out **Auriel**! ✨ Let's make productivity simpler and smarter together.