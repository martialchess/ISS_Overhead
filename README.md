# 🛰️ ISS Overhead Notifier

A small Python project that alerts you via email when the International Space Station (ISS) is above your location **and** it's nighttime (so you can actually see it).  

It checks the ISS position using the [Open Notify API](http://api.open-notify.org/) and sunrise/sunset times using the [Sunrise-Sunset API](https://sunrise-sunset.org/api).  
Runs every 60 seconds and notifies you if conditions are met.

---

## 🚀 Features
- Fetches live ISS coordinates  
- Fetches local sunrise & sunset times  
- Checks if ISS is within ±5° of your location  
- Only sends email when it’s dark outside  
- Runs every 60 seconds in the background  

---

## 🛠️ Setup

1. Clone this repo:
   ```bash
   git clone https://github.com/martialchess/ISS-Overhead.git
   cd iss-overhead-notifier

2. Create a virtual environment (optional but recommended):
   python -m venv venv
   source venv/bin/activate   # macOS/Linux
   venv\Scripts\activate      # Windows

3. Install dependencies:
   pip install -r requirements.txt

4. Update the following in main.py:
   MY_EMAIL = "your_email@example.com"
   PASSWORD = "your_email_password"
   MY_LAT = 31.520370   # your latitude
   MY_LONG = 74.358749  # your longitude

5. Run the app:
   python main.py

6. Requirements

   Python 3.x

   requests

   pandas (if used elsewhere)

   SMTP-compatible email account (e.g., Gmail)

7. Install them via:
   pip install -r requirements.txt

📧 Email Notes

   If using Gmail, you may need to generate an App Password instead of using your regular password.

   Make sure to enable Less Secure Apps / App Passwords and 2FA depending on your account setup.

🔥 Example

   When the ISS is overhead at night, you’ll get an email like:

   Subject: Look Up!

   The ISS is above you in the sky right now!

