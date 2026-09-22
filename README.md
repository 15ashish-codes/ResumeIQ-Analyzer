# ResumeIQ Frontend

Responsive Bootstrap 5 frontend for the ResumeIQ AI Resume Analyzer.

## Included
- Landing page
- Login / registration / password reset UI
- Dashboard with Chart.js analytics
- Drag-and-drop PDF/DOCX upload
- Frontend analysis result demo
- Job-description matching UI
- ATS resume builder with browser print-to-PDF
- Recruiter portal
- Admin panel
- Profile settings
- Dark/light mode
- API helper prepared for Django REST Framework JWT endpoints

## Run
No Node.js is required for this frontend.

1. Extract the ZIP.
2. Open `index.html` directly, or serve the folder with a local static server:
   - VS Code Live Server / Live Preview
   - Python: `python -m http.server 5500`
3. Visit `http://127.0.0.1:5500/`.

## Django integration
The API helper defaults to:
`http://127.0.0.1:8000/api`

Change it in browser localStorage:
`localStorage.setItem('resumeiq_api_base','http://127.0.0.1:8000/api')`

Expected JWT endpoint used by the login form:
`POST /api/auth/token/`
with `{ "email": "...", "password": "..." }`

The UI currently has a graceful frontend-demo fallback so you can demonstrate the screens before the Django backend is connected. Replace demo handlers in `assets/app.js` with your DRF calls when the backend is ready.
