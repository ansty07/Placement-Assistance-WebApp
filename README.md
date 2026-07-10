# 🎯 AptiQ

**Your placement companion** — a self-contained, single-file web app for running mock aptitude and placement assessments from any JSON question set.

🔗 **Live Demo:** [aptiq-placementassistance-webapp.vercel.app](https://aptiq-placementassistance-webapp.vercel.app/)

## 📸 Home Page

<img width="1897" height="867" alt="image" src="https://github.com/user-attachments/assets/dadccece-206d-41d3-96c2-d12c828d1c4c" />




## 🧭 Overview

AptiQ is a browser-based assessment platform built as a single `index.html` file with no backend or build step required. You bring your own question set as JSON (upload a file or paste it directly), and AptiQ turns it into a full timed, proctored, exam-style test experience — complete with a detailed performance dashboard at the end.

## ✨ Key Features

### 📂 Flexible Question Loading
- Upload a `.json` file via drag-and-drop or file picker
- Paste JSON directly into a text area
- Built-in sample question set to preview the expected format
- Validates structure and previews the assessment (title, question count, categories, duration) before loading

### ⚙️ Pre-Assessment Options
- ⛶ **Fullscreen mode** — expands the test to fill the screen (exit anytime with Esc)
- 📷 **Camera & mic proctoring** — optional webcam/mic verification with a live preview and "Secure Mode" indicator during the test

### 📝 Exam Experience
- Countdown timer with warning and danger states as time runs low
- Auto-submit when time expires
- Question palette showing answered, flagged, and current questions at a glance
- Per-question confidence rating (Very confident / Somewhat / Not sure)
- Flag questions for later review
- Keyboard shortcuts (arrow keys to navigate, `F` to flag, `1`/`2`/`3` for confidence)
- Submit confirmation modal showing answered/unanswered/flagged counts

### 📊 Results Dashboard
- Overall score with an animated readiness ring and readiness badge (Excellent / Good / Needs Improvement)
- Category-by-category accuracy breakdown
- Performance split by difficulty (Easy / Medium / Hard)
- Confidence calibration analysis — flags overconfidence and underconfidence patterns
- Overconfident mistakes callout — highlights questions marked "Very Confident" but answered incorrectly
- Personalized recommendations based on performance patterns
- Strengths vs. focus-area breakdown
- Expandable per-question review with correct answers and explanations
- Download results as JSON or as a printable HTML report
- Remembers your most recent attempt and shows it on the home screen

## 🧩 Question JSON Format

```json
{
  "assessment_title": "Frontend Fundamentals Check",
  "company_name": "Sample Co.",
  "duration_minutes": 10,
  "questions": [
    {
      "category": "JavaScript",
      "difficulty": "easy",
      "question": "What does `typeof null` return in JavaScript?",
      "options": ["'null'", "'object'", "'undefined'", "'number'"],
      "correct_answer": "'object'",
      "explanation": "This is a long-standing quirk of JavaScript..."
    }
  ]
}
```

Only a `questions` array is required — AptiQ falls back to sensible defaults for the rest.

## 🛠️ Technologies Used

- **HTML5 / CSS3** — single-file layout with custom properties, glassmorphism panels, and 3D tilt-on-hover cards
- **Vanilla JavaScript** — no frameworks or dependencies
- **Google Fonts** — Montserrat, JetBrains Mono, Space Grotesk, Syne, Fredoka, Allura
- **MediaDevices API** — for optional camera/mic proctoring
- **Fullscreen API** — for distraction-free test mode
- **localStorage** — persists the most recent result between sessions

## 🚀 Getting Started

1. Open `index.html` in any modern browser — no installation or server needed
2. Upload a `.json` question set, paste one in, or load the sample
3. Review the assessment summary and hit **Continue**
4. Configure fullscreen/proctoring options and **Start assessment**
5. Answer questions, rate your confidence, flag anything to revisit
6. Submit to view your full results dashboard

## ⚠️ Disclaimer

AptiQ is a practice tool for self-assessment and placement preparation. Scores and readiness labels are generated locally from your own question set and are not affiliated with or endorsed by any hiring company.

---

*Created by Anshuman Mohanty & Tridev Ashirbad Dash*
