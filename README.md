# FlaskAuthApp

A simple Flask-based authentication system with user registration, login, and dashboard functionality.

---

## The Bug

When users try to register without entering their name, email, or password, the form goes through anyway. That's obviously wrong — we need to catch empty fields before they hit the database.

## What Needs to Be Done

### 1. Fix Registration Validation

The `/register` route needs proper server-side checks:

- Name can't be blank
- Email can't be blank  
- Password can't be blank
- No duplicate emails allowed (show an error if email exists)
- Password must be 6+ characters

Show clear error messages when something's wrong.

**Important:** HTML `required` attributes aren't enough here. Flask must validate on the backend.

### 2. Push to GitHub

- Make the repo public
- Include this README

### 3. Deploy on Render

- App should run without crashing
- Validation should work on the live site
- URL needs to be accessible

### 4. Submission

Fill out the Google Form with:
- Name
- Roll Number
- Section
- GitHub repo link
- Render URL

---

## Running Locally

```bash
pip install -r requirements.txt
python app.py
```

Then open `http://localhost:5000` in your browser.
