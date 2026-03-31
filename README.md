# NSCT Preparation Suite 🚀

A comprehensive, digital MCQ practice dashboard for IT Graduates preparing for the **National Skill Competency Test**.

## 📂 Project Structure
- `index.html`: The main dashboard and quiz engine.
- `syllabus/`: Contains JSON files for each of the 10 competency areas.
  - `web-dev.json`: (10% weightage)
  - `networking.json`: (10% weightage)
  - `software-eng.json`: (10% weightage)
  - `cyber-security.json`: (5% weightage)
  - so on...

## 🛠️ How to Run (Locally)
Since the browser blocks `fetch()` requests for local files due to CORS policy, you must run this using a local server:

1. **VS Code User (Recommended):**
   - Install the **Live Server** extension.
   - Right-click `index.html` and select **"Open with Live Server"**.
2. **Python User:**
   - Open terminal in the project folder.
   - Run: `python -m http.server 8000`
   - Visit `http://localhost:8000` in your browser.

## 🤝 How to Collaborate
1. **Adding Questions:** Open the relevant `.json` file in the `syllabus/` folder and add a new object to the `questions` array.
2. **Format:**
   ```json
   {
     "id": "unique_id",
     "subtopic": "Subtopic Name",
     "question": "The question text?",
     "options": ["A", "B", "C", "D"],
     "answer": 0, // Index of the correct option (0=A, 1=B, etc.)
     "explanation": "Brief concept insight."
   }