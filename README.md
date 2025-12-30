# 🔐 Snippet Manager – QR Based Login System

A secure and modern **QR-based login system** that allows users to log in to a web application by scanning a QR code using a **Flutter mobile app**.  
This project demonstrates real-time authentication using **Firebase Firestore** with seamless communication between **Web (GitHub Pages)** and **Mobile (Flutter)**.

---

## 🚀 Project Overview

The system works in three parts:

1. **Web App (Frontend)**  
   - Generates a unique QR code
   - Listens for login approval in real time
   - Updates UI when QR is scanned

2. **Mobile App (Flutter)**  
   - Scans the QR code
   - Sends approval to Firebase
   - Shows loading animation → approval status

3. **Firebase (Backend)**  
   - Stores QR tokens
   - Handles real-time status updates
   - Acts as a bridge between web and mobile

---

## 🧠 How It Works

1. User opens the website  
2. Website generates a QR code with a unique token  
3. Flutter app scans the QR code  
4. App updates Firestore status → `approved`  
5. Website detects approval in real time  
6. Login is confirmed / redirected

---

## 🛠 Technologies Used

### 🌐 Web
- HTML5
- CSS3
- JavaScript
- QRCode.js
- Firebase Firestore
- GitHub Pages (Hosting)

### 📱 Mobile App
- Flutter
- Dart
- mobile_scanner package
- Firebase Core
- Cloud Firestore

### ☁ Backend
- Firebase Firestore (NoSQL, Real-time)

---

## 📦 Features

- ✅ QR-based secure login
- 🔄 Real-time authentication
- 📱 Cross-device interaction
- 🔒 No password required
- ⚡ Fast & lightweight
- 🌐 Works on GitHub Pages
- 🧪 Demo-friendly (manual redirect option)
- 🎨 Custom splash screen & app icon

---

## 🎯 Advantages

- Eliminates password-based risks
- Prevents phishing attacks
- No backend server required
- Scalable with Firebase
- Works on low-end devices
- Easy to deploy and maintain
- Industry-relevant authentication method

---

## 🖥 Compatibility

### Web
- Chrome
- Firefox
- Edge
- Mobile browsers

### Mobile
- Android (tested)
- iOS (supported by Flutter)

### Hosting
- GitHub Pages ✅
- Netlify ✅
- Firebase Hosting ✅

---

## 📁 Project Structure

```text
Snippet-Manager/
│
├── index.html
├── dashboard.html
│
├── assets/
│   └── logo.png
│
├── flutter_app/
│   ├── lib/
│   │   └── main.dart
│   ├── android/
│   ├── pubspec.yaml
│   └── assets/
│       └── logo.png
```
---

## 🔐 Firebase Collections

### `qr_login`
```json
{
  "status": "pending | approved",
  "createdAt": "timestamp"
}
