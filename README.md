# ResumeLab — AI Resume Analyzer

A small Node.js web app that compares resume text with a target job description and returns constructive feedback using the OpenAI Responses API.

## Deploy

This repository includes a Render Blueprint. In Render, create a new Blueprint from this GitHub repository. The blueprint uses the `server.mjs` folder as the service root and defines the start command and health check. Add `OPENAI_API_KEY` as a private Render environment variable before using AI analysis. Never commit the API key.

## Local run

Install Node.js 20+, copy `.env.example` to `.env` in the app folder, add your API key, run `node server.mjs`, then open `http://localhost:3000`.

## Privacy and limits

The app does not store resumes in a database. Resume text is sent to the app server and OpenAI to create the requested feedback. The demo has an in-memory limit of five AI analyses per IP per minute; counters reset when the server restarts. It is not an employment decision system.
