
# 🗳️ Secure Face Recognition Voting System

A **web-based voting platform** built using **Flask**, leveraging **facial recognition** for secure and verifiable voter authentication. This system aims to eliminate fraudulent voting, ensure one-person-one-vote enforcement, and provide real-time election analytics — all through a modern, easy-to-use interface.

---

## ✅ Key Features

- **Facial Recognition Authentication**: Voters must verify their identity using their face before voting.
- **One Vote per User**: Users can vote only once — further access is blocked after successful submission.
- **Admin Dashboard**: Admins can log in, manage candidates (add/delete), and view real-time vote counts.
- **Age Verification & Aadhaar/Voter ID Validation**: Ensures only valid voters above 18 years can register.
- **Secure Registration**: Users register with their credentials and facial image for later verification.
- **Real-time Results**: Displays live vote tallies and candidate rankings to both users and admins.
- **Mobile Friendly UI**: Optimized with Bootstrap for a responsive experience across devices.

---

## 🧰 Tech Stack

- **Frontend**: HTML, CSS (Bootstrap), JavaScript (Jinja2 templating)
- **Backend**: Python, Flask, SQLite
- **Facial Recognition**: OpenCV, `face_recognition`, dlib
- **Security**: Password hashing (`werkzeug.security`), session handling

---

## 📁 Folder Structure

```
voting-system/
│
├── static/
│   ├── css/ (Custom styles)
│   ├── faces/ (Stored face images)
│   ├── uploads/ (Candidate logos)
│
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── register.html, login.html, face_verify.html, vote.html, result.html
│   └── admin_dashboard.html, admin_login.html
│
├── app.py
├── facial_recognition.py
├── init_db.py
├── voting_system.db
```

---

## 🚀 How to Run

```bash
# Create virtual environment
python -m venv frenv
source frenv/bin/activate  # or frenv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Initialize database
python init_db.py

# Run the app
python app.py
```

---

## 📌 Future Improvements

- Email/OTP verification for account recovery  
- Liveness detection to prevent spoofing  
- Exportable results and logs  
- Multi-region voting support
