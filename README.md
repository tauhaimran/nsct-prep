# NSCT Preparation Suite 🚀

A comprehensive, digital MCQ practice dashboard for IT Graduates preparing for the **National Skill Competency Test (NSCT)**.

## 📂 Project Structure
- `index.html`: Main interactive dashboard and quiz engine.
- `syllabus/`: Topic-wise question banks (10 core areas).
- `custom-mocks/`: Custom timed mock test definitions.
  - `custom-test-template.json`: Template for authoring your own mock test set.
  - `custom-test.json`: Example custom mock with sample questions.

## 🧭 NSCT Syllabus (Core Areas + Weightage)
- Problem Solving & Analytical Skills (20%)
- Web Development (10%)
- Programming (C++/Java/Python) (10%)
- Data Structures & Algorithms (10%)
- Networking & Cloud (10%)
- Database Systems (10%)
- AI/ML & Data Analytics (10%)
- Software Engineering (10%)
- Operating Systems (5%)
- Cyber Security (5%)

## 🚀 Run the App Locally
The app uses `fetch()` for JSON assets, so a local server is required.

1. **VS Code (recommended)**
   - Install **Live Server** extension.
   - Right-click `index.html` → **Open with Live Server**.
2. **Python**
   - Open terminal in project folder.
   - Run: `python -m http.server 8000`
   - Open: `http://localhost:8000`

## 🛠️ Usage Guide
1. Launch and confirm dashboard loads with topic cards and global progress.
2. Use sidebar options:
   - `Dashboard Overview` (default)
   - `Timed 2hr Mock Test`
   - `Browse All MCQs`
   - `Credits`

### Timed Mock Test (2 hours)
- Click `Timed 2hr Mock Test`.
- Choose between:
  - `Start Random Syllabus Mock` (auto picks from all `syllabus/*.json` questions)
  - `Start Custom Mock` (reads `custom-mocks/custom-test.json`)
- Timer starts at **120:00**.
- Answer questions with immediate feedback and explanation.
- Score shown at completion or when time expires.

### Custom Mock Test File Format
Create/edit `custom-mocks/custom-test.json` (copy from template):
```json
{
  "title": "Custom 2hr Mock Test",
  "questions": [
    {
      "id": "cust_001",
      "subtopic": "Subtopic Name",
      "question": "Question text?",
      "options": ["A", "B", "C", "D"],
      "answer": 0,
      "explanation": "Why this is correct.",
      "tags": ["tag1", "tag2"]
    }
  ]
}
```

### Browse All MCQs
- Click `Browse All MCQs`.
- Filter by topic/subtopic and search by keyword.
- Expand each question to view options, correct answer, and explanation.

### Credits
- Click `Credits` for author details and links.
- Includes GitHub, Tumblr, LinkedIn, and email.

## 📦 Add/Update Questions
- Add objects into `syllabus/{area}.json` under `questions`.
- Required: `id`, `subtopic`, `question`, `options`, `answer`, `explanation`.
- Optional: `tags` (used for library search).

## 💡 Developer Notes
- Progress is stored in localStorage key: `nsct_v2_progress`.
- `state.allQuestions` is built from all syllabus files at startup.
- Mock mode supports random syllabus pool and custom static dataset.

## 👨‍💼 Creator
**Tauha Imran**
- VR Developer, CS (FAST-NUCES Islamabad)
- GitHub: https://github.com/tauhaimran
- Tumblr: https://www.tumblr.com/raggygaggy
- LinkedIn: https://www.linkedin.com/in/tauha-imran-6185b3280/
- Email: tauhimran@gmail.com
- Portfolio: https://tauhaimran.github.io/
- YouTube: https://www.youtube.com/@RaggyGaggy

---

Official NSCT syllabus reference: https://nsct.hec.gov.pk/
