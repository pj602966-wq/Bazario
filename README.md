# 🛒 Bazario | Full-Stack Mobile Shopping Ecosystem

Bazario is a modern, mobile-first Web App (PWA) designed to connect local customers with sellers. It features real-time order tracking, GPS location detection, and a secure PIN verification system for deliveries.

## 📱 Features

### Customer App (`mainv3.1.html`)
* **Real-time Product Browsing:** View live products synced with Firebase.
* **Smart Cart:** Add multiple items and calculate totals.
* **Live GPS Tracking:** Captures delivery coordinates and address.
* **Order History & Timer:** 24-hour countdown for every order placed.
* **PIN Generation:** Automatic 4-digit security code for safe delivery.

### Seller Dashboard (`sellerv3.3.html`)
* **Live Order Alerts:** Receive customer address and phone number instantly.
* **Revenue Analytics:** Tracks total earnings from completed sales.
* **Product Management:** Add, edit, or delete products with Pinterest image links.
* **PIN Verification:** Securely complete orders by entering the customer's PIN.

## 🛠️ Tech Stack
* **Frontend:** HTML5, Tailwind CSS, Lucide Icons.
* **Backend:** Firebase Firestore (NoSQL Database).
* **Auth:** Firebase Authentication (Email/Password).
* **PWA:** Service Workers and Manifest.json for mobile installation.

## 🚀 Installation & Setup
1. **Clone the Repo:** Upload these files to your GitHub repository.
2. **Firebase Config:** * Create a project at [Firebase Console](https://console.firebase.google.com/).
   * Enable **Firestore** and **Authentication**.
   * Replace the `firebaseConfig` object in both HTML files with your unique keys.
3. **Hosting:** Enable **GitHub Pages** in your repository settings to go live.

## 🛡️ Security Rules
To protect your data, use the following Firestore rules:
```javascript
match /databases/{database}/documents {
  match /{document=**} {
    allow read, write: if request.auth != null;
  }
}
