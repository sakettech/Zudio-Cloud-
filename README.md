Zudio: Next-Gen O2O Retail Experience 🛍️☁️



Bridging the gap between offline stores and digital convenience using Web Technologies, Real-time Cloud Sync, and AI.

🚀 Overview

The Zudio Next-Gen App is a responsive, progressive web-based application designed to revolutionize the brick-and-mortar shopping experience. Built for the MLH Hacktoberfest Hack Day - Dehradun, this project introduces an Online-to-Offline (O2O) ecosystem featuring Self-Checkout Scanners, dynamic Loyalty Programs (Z-Coins), and a live AWS-inspired Admin Dashboard.

🎯 Problem Statement

Traditional retail shopping faces several friction points:

Long billing queues during peak hours/weekends.

Disconnected online and offline customer loyalty experiences.

Lack of real-time inventory and customer measurement tracking for retail admins.

💡 The Solution

We built a seamless, lightweight web application that allows users to walk into a physical Zudio store, scan items via their smartphone camera, apply dynamic loyalty coins, and pay securely via Razorpay—bypassing the billing counter entirely.

✨ Key Features

📷 Scan & Go (Self Check-In): Integrates HTML5 getUserMedia API to turn the user's browser into a barcode scanner for instant in-store checkouts.

🪙 Z-Coins Loyalty Engine: Custom algorithmic reward system where users earn and redeem coins (10 Coins = ₹1) with upper-bound limit validations.

💳 Secure External Checkout: Integrated Razorpay test gateway for seamless UPI/Card transactions.

📍 Smart Store Locator: Direct Google Maps API integration fetching geolocation data to route users to the nearest Dehradun Zudio outlets.

☁️ Live Enterprise Admin Console: An AWS-styled dashboard featuring 5-second polling (Real-time sync) with Google Sheets via Apps Script (doGet/doPost), complete with skeleton loaders and inline editing.

🏆 Hackathon Tracks Targeted

This project is built to align with the prize categories for the MLH Dehradun Hack Day:

1. Best Use of Gemma 4 (DeepMind Google)

Implementation Plan: We are integrating a "Gemma 4 AI Styling Assistant" into the app. By passing the user's saved measurements (Chest, Shoulder, Fit) and the item they just scanned to the Gemma 4 open-weight model via the Gemini API, the app provides real-time, personalized size recommendations and fashion advice (e.g., "Based on your profile, size M will give you the perfect oversized look").

2. Best Open-Source AI Project (DigitalOcean)

Implementation Plan: The complete source code is open-sourced on GitHub. The backend data pipelines and AI model inference logic are designed to be deployed seamlessly on DigitalOcean droplets, making the retail infrastructure highly scalable for open-source retail developers.

💻 Tech Stack

Frontend: HTML5, CSS3 (Custom Properties & Animations), Vanilla JavaScript (ES6+).

Backend / Database: Google Sheets API via Google Apps Script (Serverless Webhook approach).

Payments: Razorpay Checkout SDK.

APIs & Libraries: HTML5 MediaDevices API (Camera), FontAwesome (Icons), Google Maps URI links.

⚙️ Local Setup & Installation

Follow these steps to run the application locally:

Clone the repository:

git clone https://github.com/your-username/zudio-nextgen.git
cd zudio-nextgen


Run a local server:
Since the app uses module imports, localStorage, and the Camera API, it needs to be run on a local server (not directly from the file system).

Using Python:

python -m http.server 8000


Using Node.js (Live Server):

npx live-server


Open in Browser:
Navigate to http://localhost:8000/index.html

Camera Testing Note:
To test the "Scan & Go" camera feature on a mobile device, ensure you are serving the site over HTTPS, or use a tool like Ngrok for local tunneling, as modern browsers block camera access on unsecured HTTP connections.

📂 Project Structure

📦 zudio-nextgen
 ┣ 📜 index.html         # Main app interface, Trending Styles & Search overlay
 ┣ 📜 bag.html           # Dynamic shopping cart, Z-Coin engine & Razorpay integration
 ┣ 📜 profile.html       # User dashboard, Camera Scanner, Store Locator & Auth
 ┣ 📜 admin.html         # Live AWS-style Admin Console with real-time polling
 ┗ 📜 README.md          # Project documentation


🚀 Future Roadmap

[ ] Complete Gemma 4 Multimodal integration for AI Outfit Generation based on scanned items.

[ ] Migrate Google Sheets Database to a scalable PostgreSQL database hosted on DigitalOcean.

[ ] Implement WebSockets for 0-latency admin dashboard updates.

[ ] PWA (Progressive Web App) conversion for offline accessibility.
