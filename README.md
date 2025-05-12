# 📘 Google Workspace Integration (ASP.NET Core MVC)

This ASP.NET Core MVC project integrates with **Google Workspace APIs** to demonstrate the use of Google OAuth 2.0 authentication, Google Sheets API, and Gmail API. It allows a user to log in with Google, read data from a Google Sheet, and send emails using their Gmail account.

---

## 🚀 Features

- 🔐 Google OAuth 2.0 Login
- 📊 Display first 5 rows from a Google Sheet
- 📧 Send an email using Gmail API

---

## 🛠️ Technologies Used

- ASP.NET Core 9.0 (MVC)
- Google.Apis.Gmail.v1
- Google.Apis.Sheets.v4
- OAuth 2.0 with Google
- Visual Studio Code (Mac compatible)

---

## 📁 Project Structure

- **Controllers/**
  - `GoogleAuthController.cs` – Handles Google login callback
  - `GoogleSheetsController.cs` – Fetches and displays data from Sheets
  - `GoogleGmailController.cs` – Sends email using Gmail API
  - `HomeController.cs` – Default app views
- **Services/**
  - `GoogleSheetsService.cs` – Contains logic to read Sheets
  - `GoogleGmailService.cs` – Contains logic to send Gmail
- **Views/**
  - Razor pages for Sheets display and email form

---

## ⚙️ Setup Instructions

### 1. Configure Google Cloud Project
- Go to [Google Cloud Console](https://console.cloud.google.com)
- Create a new project and enable:
  - Google Sheets API
  - Gmail API
- Create **OAuth 2.0 credentials**
  - Authorized redirect URI: `https://localhost:5109/signin-google`

### 2. Update `appsettings.json`

```json
"Authentication": {
  "Google": {
    "ClientId": "YOUR_CLIENT_ID",
    "ClientSecret": "YOUR_CLIENT_SECRET"
  }
},
"Google": {
  "SpreadsheetId": "YOUR_SPREADSHEET_ID"
}
### 3. Run the Project
dotnet restore
dotnet build
dotnet run
