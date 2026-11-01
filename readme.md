# BuilderAI

BuilderAI is an AI-powered web app builder that turns a natural-language idea into a working website or landing page. Users can describe the product they want, generate a project, iterate on it through chat, preview the app live, publish it, and download the generated code as a ZIP.

## Overview

This project combines a React frontend with an Express backend and an AI generation pipeline. The experience is designed to feel like an intelligent app builder:

- Create a new project from a prompt
- Chat with the AI to revise or improve the generated app
- Inspect and edit generated project files
- Preview the website in-browser
- Publish the site and share it publicly
- Download the generated project for local use

## Tech Stack

### Frontend
- React + Vite
- React Router
- Tailwind CSS
- Lucide icons

### Backend
- Node.js + Express
- MongoDB with Mongoose
- JWT-based authentication
- OpenRouter/AI integration for generation and chat

## Features

- User authentication and session handling
- Project dashboard for managing multiple generated apps
- Prompt-based AI creation flow
- File explorer for generated project structure
- Live preview and code viewing
- Project revision via conversational chat
- Publish flow for generated sites
- Download project ZIP archive

## Project Structure

```text
builder-ai/
├── client/                 # React frontend
│   ├── src/
│   ├── public/
│   └── package.json
├── server/                 # Express API and AI services
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── .env
│   └── package.json
├── .gitignore
├── readme.md
└── package.json (if added at repo root)
```

## Getting Started

### 1. Install dependencies

Frontend:

```bash
cd client
npm install
```

Backend:

```bash
cd server
npm install
```

### 2. Configure environment variables

Create or update `server/.env` with values such as:

```env
JWT_SECRET="your_jwt_secret"
ORIGINS="http://localhost:5173,http://localhost:3000"
MONGODB_URI="mongodb://localhost:27017/builderai"
OPENROUTER_API_KEY="your_openrouter_key"
OPENROUTER_MODEL="openai/gpt-4o-mini"
```

### 3. Run the app

Start the backend:

```bash
cd server
npm run dev
```

Start the frontend:

```bash
cd client
npm run dev
```

Then open the client in the browser, usually at:

```text
http://localhost:5173
```

## Typical Workflow

1. Register or log in to the application.
2. Enter a prompt such as "Create a portfolio website for a freelance designer".
3. Wait for the AI to generate the project structure and code.
4. Review the app in the builder preview.
5. Use chat to request design, content, or functionality changes.
6. Publish the app or export the project files.

## Notes

- The app uses an AI model through OpenRouter, so a valid API key is required for generation features.
- MongoDB must be available for user and project persistence.
- This project is designed for experimentation and product prototyping, not as a production-ready deployment template without additional hardening.

## License

This project currently does not define a license in the repository metadata. Add a license file and update this section if you intend to distribute it publicly.
