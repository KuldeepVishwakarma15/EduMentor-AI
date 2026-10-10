# EduMentor AI — Student Dropout Prevention & Smart Learning Assistant 🎓🚀

EduMentor AI is an AI/ML-powered early warning and student retention platform designed to help institutions, counselors, and students identify dropout risk early, understand the causes behind it, and take timely action.

The system combines predictive analytics, explainable AI, intervention tracking, and a bilingual mentor experience to support academic success and student retention.

---

## Key Features

1. Executive Overview & Analytics
   - Institutional dropout risk metrics for high, medium, and low risk groups
   - Interactive charts with monthly and weekly views
   - Driver analysis covering attendance, academic performance, fee clearance, distance, and backlogs

2. At-Risk Student Roster
   - Student summary list with live risk scores and category tags
   - Search by name, roll number, or department
   - Filtering by risk level and academic branch
   - CSV export support for administrative reporting

3. Student Profile & What-If Risk Simulator
   - Detailed student profile with attendance metrics, SGPA/CGPA history, and fee status
   - Explainable AI insights using SHAP-inspired factors
   - Interactive simulation sliders for attendance, study hours, and backlog conditions
   - Counseling intervention logging and follow-up tracking

4. Self-Registration & Student Login
   - Students can register their academic and financial information directly
   - Risk prediction is generated immediately after form submission
   - App automatically switches the user role to Student and loads the personal profile view
   - Data is saved in localStorage for persistence across refreshes

5. Bilingual AI Mentor
   - AI-powered mentor experience using the Gemini API
   - Supports English and Hindi/Hinglish conversations
   - Provides counseling guidance, recovery plans, mental wellness support, and scholarship-related recommendations

---

## Tech Stack

- Frontend: React 19, TypeScript, Tailwind CSS v4, Lucide Icons, Motion
- Backend: Node.js, Express, tsx
- AI/LLM: IBM watsonx AI and Google Gemini via `@google/genai`
- Bundler: Vite

---

## Getting Started

### 1. Prerequisites
- Node.js 18+ or 20+
- npm or bun
- IBM watsonx AI API for mentor chat functionality

### 2. Install Dependencies

Open a terminal in the project folder and run:

```bash
npm install
```

### 3. Create Environment Variables

Create a `.env` file in the project root by copying `.env.example`:

```bash
cp .env.example .env
```

Add your IBM watsonx AI API:

```env
GEMINI_API_KEY=your_actual_gemini_api_key_here
PORT=3000
```

> Note: If no IBM watsonx AI API key is provided, the core application features such as dropout prediction, student records, charts, and self-registration will still work. The AI Mentor chat feature requires a valid IBM watsonx AI API key and configuration.

### 4. Run the Development Server

```bash
npm run dev
```

Then open the app in your browser:

`http://localhost:3000`

### 5. Production Build

```bash
npm run build
npm start
```

---

## Project Structure

This is the actual project structure currently used in this repository:

```text
bharat-cares-app/
├── .env.example
├── .gitignore
├── README.md
├── index.html
├── metadata.json
├── package-lock.json
├── package.json
├── server.ts
├── tsconfig.json
├── vite.config.ts
├── src/
│   ├── App.tsx
│   ├── index.css
│   ├── main.tsx
│   ├── components/
│   │   ├── AIMentorChatView.tsx
│   │   ├── AddStudentRecordModal.tsx
│   │   ├── AtRiskRosterView.tsx
│   │   ├── EDAStudioView.tsx
│   │   ├── Header.tsx
│   │   ├── OverviewView.tsx
│   │   ├── RiskSparkline.tsx
│   │   └── StudentProfileView.tsx
│   └── data/
│       ├── modulesContent.ts
│       └── uciStudents.ts
└── node_modules/   # Installed dependencies
```

---

## Quick Tips

- Use the sidebar role switcher to switch between Dean, Counselor, and Student views.
- Use the Add / Register My Record option to create a new student profile and generate an instant risk score.
- The student risk simulator lets you test different attendance and academic scenarios without changing the stored data.

---

## License

MIT License.

Created for the AICTE-IBM Bharat Cares Educational Initiatives.
