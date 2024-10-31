
# 🌟 Auriel - Your AI Productivity Companion 🌟

Welcome to **Auriel**, an AI-driven assistant designed to be your second brain. Imagine an app that helps you track your classes, organize your tasks, remember your ideas, and even assist you with emails—all tailored to your unique preferences. Auriel is built to boost your productivity, offering intuitive reminders and intelligent suggestions, so you can focus on what matters most.

> **Note:** Auriel is in the early stages of development, so you’ll see the foundation here for a project designed to grow! Your contributions, ideas, and feedback are warmly welcomed. ❤️

---

## 📜 App Description

**Auriel** is a personal productivity assistant with a twist. Combining AI with integrated task management, it’s your digital partner for managing day-to-day tasks, logging ideas, and sending reminders just when you need them. Think of it as a **“second brain”** that captures details, organizes them intuitively, and offers you the peace of mind to focus on the bigger picture.

With Auriel, you’ll experience:

- **Class and Task Management**: Sync your schedule, receive reminders for tasks, and never miss a deadline.
- **Smart Email Assistant**: Get AI-generated drafts for emails and reminders about follow-ups.
- **Idea Logging and Reminders**: Log your ideas on the go, and let Auriel remind you to revisit them.
- **Daily Summaries**: Start your day with a rundown and end it with a wrap-up, so you’re always on track.
- **Customization Options**: Set up preferences, communication tone, and even meal planning ideas!

Auriel’s vision is to make daily organization feel effortless, leaving you more time for creativity and focus.

---

## 🚀 Features

### 🌅 Phase 1 - Minimum Viable Product (MVP)
Core functionality to help you get started with Auriel:

- **🗓 Class Management**: Integrates with Google Calendar to track your classes.
- **🔔 Task Reminders**: Sends you reminders after each class to add related tasks.
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

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/your-username/Auriel.git
   cd Auriel
   ```

2. **Firebase Setup**:
   - Create a Firebase project, enable **Firestore** and **Authentication**.
   - Download the `GoogleService-Info.plist` file and add it to the `frontend/` directory in Xcode.

3. **Google API Setup**:
   - Enable **Google Calendar** and **Gmail API** in the [Google Cloud Console](https://console.cloud.google.com/).
   - Set up OAuth 2.0 credentials and download the file.
   - Place the credentials in `backend/functions/` and configure `calendar.js` and `email.js`.

4. **Install Firebase CLI**:

   ```bash
   npm install -g firebase-tools
   firebase login
   firebase init
   ```

   - Select **Functions** during setup and add Firebase config to `backend/firebase.json`.

5. **Install Backend Dependencies**:

   ```bash
   cd backend/functions
   npm install
   ```

6. **Deploy Firebase Functions**:

   ```bash
   firebase deploy --only functions
   ```

7. **Run the iOS App**:
   - Open `Auriel.xcodeproj` in Xcode.
   - Select a simulator or physical device and click **Run**.

---

## 📂 Project Structure

```plaintext
Auriel/
├── frontend/                     # SwiftUI iOS App Code
│   ├── Auriel.xcodeproj/         # Xcode project files
│   ├── Assets/                   # Assets (icons, images, etc.)
│   ├── Models/                   # Data models (e.g., User, Task, Idea)
│   ├── Views/                    # UI Views (Main Dashboard, Task Screen, etc.)
│   ├── ViewModels/               # ViewModels for managing state
│   ├── Services/                 # API services (e.g., Google Calendar API)
│   ├── Utils/                    # Utility functions
│   └── App.swift                 # Main app file
│
├── backend/                      # Backend Code
│   ├── functions/                # Firebase Cloud Functions
│   │   ├── index.js              # Main functions entry point
│   │   └── api/                  # Subfolder for specific APIs
│   │       ├── calendar.js       # Google Calendar functions
│   │       ├── email.js          # Gmail functions
│   │       ├── notifications.js  # Notification-related functions
│   └── firebase.json             # Firebase configuration file
│
├── docs/                         # Documentation and assets for the repo
│   ├── api_documentation.md      # API endpoints and usage details
│   ├── design/                   # Screenshots, wireframes, Figma exports
│   └── user_personas.md          # Descriptions of user personas and use cases
│
├── .gitignore                    # Files to ignore in git
├── README.md                     # Main documentation for the repo
├── LICENSE                       # License for the project
└── CONTRIBUTING.md               # Contribution guidelines
```

---

## 🧰 Tech Stack

- **Frontend**: SwiftUI for iOS UI components
- **Backend**: Firebase (Firestore, Authentication, Cloud Functions)
- **APIs**: Google Calendar, Gmail, OpenAI GPT for AI responses
- **Push Notifications**: Firebase Cloud Messaging (FCM)

---

## 📡 APIs Used

1. **Google Calendar API**: Imports and manages class schedules.
2. **Google Tasks API**: Allows task addition and reminders.
3. **Gmail API**: Detects and drafts responses for relevant emails.
4. **OpenAI GPT API**: Contextual task prompts, email responses, and reminders.

---

## 📝 Contributing

Contributions are what make the open-source community such a great place! Here’s how you can help:

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

If you have any questions, suggestions, or just want to say hi, feel free to open an issue or connect with me. Auriel is an evolving project, and your insights are invaluable to making it a truly helpful “second brain” for productivity!

---

Thank you for checking out **Auriel**! ✨ Let's make productivity simpler and smarter together.
