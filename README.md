# 📸 Photobooth SaaS & Desktop Kiosk

> **⚠️ Disclaimer**  
> Full source code for this project is stored in a private repository due to an NDA with the client. This repository serves as an **architectural showcase** and case study of the system I developed as a Freelance Full-Stack Developer. I’m happy to discuss the technical details, architecture, state management, and hardware integration during an interview.

## 🖥️ SaaS Admin Dashboard Preview

![Photobox SaaS Admin Dashboard Preview](product_example.jpg)

*A fully responsive SaaS management dashboard built with TypeScript and Tailwind CSS, designed for Admin and Superadmin to monitor revenue, active sessions, and hardware status in real-time.*

## 📖 Project Overview

This project is a **hybrid SaaS + Desktop Kiosk** application for managing and operating photobooth machines. It combines modern web technologies for the cloud-based admin dashboard with a lightweight desktop application that runs directly on Windows-based kiosk machines.

The system enables seamless hardware integration, real-time image processing, secure cloud synchronization, and easy remote monitoring by administrators.

## 🛠️ Tech Stack & Architecture

- **Frontend (SaaS & Kiosk UI):** React, Next.js, TypeScript, Tailwind CSS
- **Desktop Wrapper:** Tauri (Rust) – lightweight and secure alternative to Electron
- **Backend & Database:** Supabase (PostgreSQL) + REST APIs
- **Target Environment:** Windows-based Kiosk Machines

## ✨ Key Features

### 1. Type-Safe SaaS Admin Dashboard
Built with **TypeScript** and **Tailwind CSS** to deliver a clean, highly responsive, and maintainable admin interface for monitoring revenue, machine status, and session analytics.

### 2. Hybrid Desktop Kiosk Application
The kiosk interface is wrapped using **Tauri**, allowing the React frontend to securely interact with the local file system, camera hardware, and printer while maintaining excellent performance and a small memory footprint.

### 3. Streamlined Role-Based Access
Simplified to only **Admin** and **Superadmin** roles. The desktop kiosk version removes unnecessary complexity, giving operators a focused and secure environment to manage sessions and machine settings.

### 4. Secure Machine Activation System
Implemented a custom activation flow for new kiosk machines. Each machine must be authenticated with the cloud backend using a strict activation code format.

#### Code Snippet: Activation Code Validation

```typescript
/**
 * Validates machine activation code against XXX-XXX format.
 * @param code - Activation code input
 * @returns boolean
 */
const validateActivationCode = (code: string): boolean => {
  const regexPattern = /^[A-Z0-9]{3}-[A-Z0-9]{3}$/;
  
  if (!code) return false;
  return regexPattern.test(code.trim().toUpperCase());
};

// Example: "A1B-C2D" → true
📈 Impact & Results
The architecture successfully delivered a scalable, reliable, and maintainable photobooth management system. The Tauri-based desktop application ensures fast local photo processing, while the Supabase backend provides secure real-time monitoring and data synchronization for administrators.

Created by Nauval Azfa Mahendra • 2026
