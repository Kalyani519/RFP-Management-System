# RFP-Management-System
AI-powered RFP management system: Create structured RFPs, manage vendors, send/receive proposals via email, parse responses with AI, and compare proposals.
# AI-Powered RFP Management System

## Overview
Single-user web app to create structured RFPs from natural language, manage vendors, send RFPs via email, receive messy vendor replies, auto-parse them with AI, and compare proposals with scoring and AI-assisted recommendations.

## Features
- RFP creation from free text via LLM to structured JSON
- Vendor management (CRUD, selection)
- Email sending via SMTP with thread token
- Email receiving via IMAP polling; AI parsing of vendor replies
- Proposal comparison with weighted scoring + AI summary/recommendation

## Tech stack
- Frontend: React (Vite), TypeScript
- Backend: Node.js (Express, TypeScript)
- Database: PostgreSQL (Prisma ORM)
- Email: Nodemailer (SMTP), ImapFlow (IMAP)
- AI: OpenAI JSON outputs validated via Zod
- Dev: Docker (optional DB), Jest (backend tests)

## Setup

### Prerequisites
- Node.js v20+
- PostgreSQL (local or via Docker)
- SMTP/IMAP mailbox credentials
- OpenAI API key

### Environment
Copy `.env.example` to `.env` and fill values.

### Backend
```bash
cd backend
npm install
npx prisma generate
npx prisma migrate dev --name init
npm run dev
