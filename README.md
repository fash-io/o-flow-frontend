
# O-FLOW

This project is a Dashboard app called **O-flow**.  
It contains the **Login page**, **2FA (OTP) modal**, and a **Biometric (dummy)** modal for future integration.  
The goal of this first phase is to establish a functional and user-friendly authentication flow that other developers can easily extend.

---

## Tech Stack

- **Frontend Framework:** React + Vite  
- **Language:** TypeScript  
- **UI Library:** ShadCN UI  
- **Icons:** Lucide React  
- **State Management:** Zustand  
- **Styling:** Tailwind CSS  

---

## Features Implemented (Week 1)

### Login Page
- Users can log in with **email + password** fields.  
- Input validation for empty or invalid fields.  
- Displays **error/success messages** during login attempts.  
- Includes **placeholders** for future OTP and Biometric authentication buttons.

### Two-Factor Authentication (2FA)
- After login, a **modal** opens requesting a 6-digit OTP.  
- The OTP is currently **static (`123456`)** for demo purposes.  
- If the entered OTP matches, the user is redirected to the dashboard.  
- Incorrect OTP shows an error message.  

### Biometric Modal (Dummy Flow)
- Simulates biometric authentication (fingerprint scan).  
- When triggered, it **automatically “authenticates” after 6 seconds**.  
- Used only for demonstration — no real biometric data is processed.

---

## ⚙️ Project Structure

```

src/
│
├── components/
│   ├── LoginForm.tsx
│   ├── TwoFA.tsx
│   ├── BiometricsModal.tsx
│
├── pages/
│   ├── Dashboard.tsx
│   └── AuthPage.tsx
│
├── store/
│   └── useAuthStore.ts
│
└── App.tsx

````

---

## Getting Started

### 1️. Clone the Repository
```bash
git clone https://github.com/alvynadams/o-flow-frontend.git
cd dashboard-auth
````

### 2️. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3️. Run the App

```bash
npm run dev
```

Then open **[http://localhost:5173/](http://localhost:5173/)** in your browser.

---

## How to Test the Flow

1. Enter any **valid email format** and **password**.
2. Click **Login** → the **OTP modal** opens.
3. Enter **`123456`** as the OTP.
4. You’ll see a **success message** and be redirected to the dashboard.
5. Alternatively, try the **Biometric modal** — it will auto-sign you in after **6 seconds**.

---

## Next Steps (Planned for Later Weeks)

* Connect authentication to real backend API.
* Implement role-based access (Admin, Employee, etc).
* Integrate real 2FA (via email/SMS).
* Secure biometric authentication flow.
* Add registration and password recovery pages.

---

