# Gemini-Powered Flask Chatbot

This project is a secure, authenticated web application built with **Flask** that provides a chat interface powered by the **OpenAI API**. It uses **JWT (JSON Web Tokens)** for stateless authentication and **Tailwind CSS** for a modern, responsive design.

---

## 🚀 Features

* **Authentication:** User login secured with JWT. The default admin user is created on startup.
* **Gemini AI Integration:** Chat functionality is powered by the `google-genai` SDK and the **`gemini-2.5-flash`** model.
* **Security:** Enforces HTTPS with an ad-hoc SSL context for local development and includes essential security headers.
* **Database:** Uses **SQLite** via Flask-SQLAlchemy for user management.
* **Environment Variables:** Configuration and secrets are managed via the `.env` file.

---

## 🛠️ Setup and Installation

### Prerequisites

* **Python 3.11+**
* The `setup.sh` script requires a Unix-like environment (Linux/macOS) or **Git Bash** on Windows.

### 1. Configure the `.env` File

Ensure your `.env` file is in the project root and contains the following necessary variables.

| Variable | Description | Example Value |
| :--- | :--- | :--- |
| `OPENAI_API_KEY` | Your **OpenAI API Key**. | `sk-xxxxxxxxxxxx` |
| `ADMIN_USER` | The username for the database. | `admin` |
| `ADMIN_PASS` | The password for the user. | `admin1234@` |
| `SECRET_KEY` | Flask session secret key. | `supersecretkey` |
| `JWT_SECRET_KEY` | JWT signing secret key. | `jwt-secret-string` |

### 2. Run the Setup Script

The `setup.sh` script handles virtual environment creation, dependency installation, database cleanup, and starting the Flask server with HTTPS.

```bash
# Make the script executable (if necessary)
chmod +x setup.sh

# Run the setup script
./setup.sh