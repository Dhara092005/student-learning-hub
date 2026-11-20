# Student Learning Hub

A web-based learning platform for students and teachers, with a digital textbook library, learning resources, and tools for tracking student progress.

## Overview

Student Learning Hub provides student and teacher pages for accessing educational materials. The project includes textbooks and other resources for grades 6–10, a resource upload flow, and basic chat and progress features.

## Features

- Student-facing and teacher-facing pages
- Textbook and learning resource listings for grades 6–10
- Teacher resource upload support
- Basic chat and progress APIs
- Resource search and filtering features in the interface

## Technology

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Node.js, Express
- **File uploads:** Multer
- **Data storage:** JSON files in the `data/` folder

> This project does not currently use MongoDB. The backend reads and writes local JSON files.

## Project Structure

```text
student-learning-hub-main/
├── data/
│   ├── chat.json
│   ├── progress.json
│   └── resources.json
├── public/
│   ├── pdfs/             # Textbooks and learning materials
│   ├── ind.html
│   ├── welcome.html
│   ├── teacher.html
│   └── frontend scripts and styles
├── uploads/              # Files uploaded through the app
├── package.json
└── server.js
```

## Requirements

- Node.js
- npm

## Run Locally

1. Open a terminal in the project folder.
2. Install the project dependencies:

   ```bash
   npm install
   ```

3. Start the server:

   ```bash
   node server.js
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

The main page is served at `/`. The project also includes student and teacher pages at `/ind` and `/teacher`.

## Data and Uploads

The application stores resource, chat, and progress data in JSON files inside `data/`. Files uploaded through the application are stored in `uploads/`.

These files are stored locally by the application. Back them up if you need to preserve data between machines.

## Notes

- Do not upload the `node_modules` folder to GitHub; it can be recreated with `npm install`.
- The app uses local JSON file storage, so it is intended for local or demonstration use unless its storage and access controls are expanded.
- The project should not be treated as a secure production system without additional authentication, validation, and security work.
