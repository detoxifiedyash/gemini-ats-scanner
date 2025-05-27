# gemini-ats-scanner
AI-powered ATS tool to analyze resumes and match them against job descriptions using Google Gemini and Streamlit.

📌 Project Title: ATS Resume Expert – Resume Analysis & Match Percentage Using Gemini AI
🔍 Overview
ATS Resume Expert is a powerful AI-based tool built with Streamlit that leverages Google Gemini API to analyze and evaluate resumes against job descriptions. It mimics the functionality of an Applicant Tracking System (ATS) and HR recruiter by:

Providing qualitative feedback on resume-job fit.

Calculating percentage match based on keyword presence.

Highlighting missing skills and keywords from resumes.

🛠️ Technologies Used
Technology	Description
Python	Core programming language used to build the logic and integrate APIs.
Streamlit	Python library for building fast and interactive web apps. Used for front-end interface.
Google Gemini API (via google.generativeai)	Powers AI content generation and intelligent resume analysis.
pdf2image + PIL	Converts PDF resumes to images for content processing by Gemini (image input supported).
dotenv	Loads sensitive credentials (e.g., API keys) securely from .env files.
Base64	Encodes image data to pass into Gemini API in acceptable format.

⚙️ Functionality
Job Description Input: Users can paste the JD directly into a text area.
Resume Upload: Upload a resume in PDF format.
Two Output Modes:
Tell Me About the Resume: Gives detailed feedback from an HR perspective.
Percentage Match: Uses ATS-like logic to give match percentage, missing keywords, and insights.

📌 How It Works
Upload a resume (PDF).
Input the job description.
Click one of the buttons:
Evaluation Mode: Simulates HR feedback.
Match Mode: Returns match % and missing keywords.
Output is powered by Gemini 1.5 Flash model, which accepts the first page of the resume as a JPEG image input for analysis.

🖼️ Sample Output
85% Match
Missing Keywords: TensorFlow, GitHub Actions, Flask
Feedback: Great profile with strengths in computer vision and ML, but lacks deployment experience...

📁 Requirements
Python 3.8+
Streamlit
PIL
pdf2image
python-dotenv
google-generativeai

🧪 To Run Locally
bash
Copy
Edit
git clone https://github.com/yourusername/ats-resume-expert.git
cd ats-resume-expert
pip install -r requirements.txt
streamlit run app.py
Make sure to add your Google Gemini API key in a .env file:

ini
Copy
Edit
GOOGLE_API_KEY=your_api_key_here
