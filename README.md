# NextHire

NextHire is a role-based career and placement support web application designed to connect students, industry recruiters, academicians, and administrators in one platform.

## Features

### Student
- Student dashboard and profile management
- Resume analysis
- Job and internship browsing
- Application tracking
- Interview preparation
- Personalized skill roadmap and learning path
- Industry challenges

### Industry / Recruiter
- Recruiter dashboard
- Post jobs and opportunities
- View and manage applicants
- Search students and review candidate profiles

### Academician
- Academician dashboard
- Student monitoring and analytics
- Curriculum projects and project-related suggestions

### Admin
- Admin dashboard
- Review and approve registered users

### Shared
- Role-based protected routes
- Authentication flow
- AI career chatbot
- Notifications
- Theme support
- Firebase / Firestore integration with mock-data support

## Tech Stack

- React
- Vite
- JavaScript
- Tailwind CSS
- React Router
- Firebase Authentication, Firestore and Storage
- Google Gemini API integration
- Chart.js
- PDF.js
- Lucide React

## Getting Started

### Prerequisites

Install the following on your computer:
- Node.js (LTS recommended)
- npm

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd nexthire
```

Replace `<YOUR_GITHUB_REPOSITORY_URL>` with your GitHub repository URL.

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a local `.env` file in the project root. You can use `.env.example` as a reference:

```bash
# Windows PowerShell
Copy-Item .env.example .env
```

Add your own valid API and Firebase configuration values to `.env` if you want to use the corresponding live services.

Environment variables used by this project include:

```env
VITE_GEMINI_API_KEY=
VITE_FIREBASE_API_KEY=
VITE_FIREBASE_AUTH_DOMAIN=
VITE_FIREBASE_PROJECT_ID=
VITE_FIREBASE_STORAGE_BUCKET=
VITE_FIREBASE_MESSAGING_SENDER_ID=
VITE_FIREBASE_APP_ID=
VITE_FIREBASE_MEASUREMENT_ID=
```

Do not commit `.env` or any file containing private credentials to GitHub. The `VITE_` prefix means values are included in the client-side app bundle, so do not put server-side secrets in these variables. Restrict API keys and configure Firebase Security Rules before deploying.

### 4. Start the development server

```bash
npm run dev
```

Vite will print a local URL (usually `http://localhost:5173`). Open that URL in your browser.

## Available Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the development server |
| `npm run build` | Build the production version |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |

## Project Structure

```text
nexthire/
├── public/                 # Public static assets
├── src/
│   ├── components/         # Shared and role-specific UI components
│   ├── context/            # Authentication and theme context
│   ├── pages/              # Admin, student, industry and academician pages
│   ├── services/            # AI, Firebase, data, notification and PDF services
│   ├── App.jsx              # Routes and application layout
│   ├── App.css
│   └── main.jsx             # React entry point
├── .env.example             # Environment variable template
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js
```

## Notes

- Some features may use mock/sample data when live services are not configured.
- Firebase Authentication, Firestore, Storage and Firebase Security Rules should be configured for your own project before production use.
- Do not publish real user data, API keys, service account files, or private configuration.

## License

No license has been specified yet. Add a license file if you want others to reuse or contribute to this project.
