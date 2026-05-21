# Music App (Fastest) - GEMINI.md

## Project Architecture
The project is split into two main components for a professional, scalable setup:
- **/backend**: A Node.js (Express) API server that acts as the middle tier between the app and Supabase.
- **/frontend**: A Flutter mobile application that consumes the backend API.

## Tech Stack
- **Frontend:** Flutter (Dart), Riverpod (State Management), GoRouter (Navigation), just_audio (Audio), http (API calls).
- **Backend:** Node.js, Express, Supabase JS Client, dotenv (Configuration).
- **Database:** Supabase (PostgreSQL).

## Backend Configuration (`/backend`)
- **Server:** Runs on port 3000.
- **Setup:**
  1. `cd backend`
  2. `npm install`
  3. Create `.env` from `.env.example` and add your `SUPABASE_ANON_KEY`.
  4. `npm start`
- **API Endpoints:**
  - `GET /api/songs`: Returns a list of all songs in the database.
  - `GET /api/songs/:id`: Returns details for a specific song.

## Frontend Configuration (`/frontend`)
- **API URL:** The app is configured to point to `http://10.0.2.2:3000/api` (standard bridge for Android emulators).
- **Setup:**
  1. `cd frontend`
  2. `flutter pub get`
  3. `flutter run`

## Secrets & Credentials
**Note: These are stored here for local environment reference only.**

- **Supabase URL:** `https://gjzopkmjhjskepqcqnvf.supabase.co` (Used in `backend/.env`)
- **Supabase Anon Key:** `sb_publishable_w92Ime8i5V8-Hb5ofycDkQ__RAJAGZX` (Used in `backend/.env`)
- **PostgreSQL Connection:** `postgresql://postgres:iloveqwertyA@123#456@db.gjzopkmjhjskepqcqnvf.supabase.co:5432/postgres`
- **Penpot MCP Token:** `eyJhbGciOiJBMjU2S1ciLCJlbmMiOiJBMjU2R0NNIn0.5f4kDwK1K9omqvQCMpbpL78YdK2ZHtZt2aY7RgGcl1qkeTSAjhibtw.MVARrUBkKxdqzq4w.Wzx_o-qBYtjrVRdJYnYRRfx6WE_7WZ8nZYAzlXaOD2ugIDOrBcFTmzFYMsKCQKCo3OKfynOy-yiPwY7FOnMvIPkhfSNlIXN2CgSeyjhNB-hORuxiIE8TlXWfDH5HEPQrXSKyWyzaVkCmYVlCgzXDjSvtjCLi3aAIxwxN9jGjP_v79JTzXHCDFNNrrnKLXHArAhuNwXMvBKrP.Wm8fABmrqFonDs4npDEvfw`
- **Backend Port:** `3000` (Used in `backend/.env`)
- **Codespaces Backend URL:** `https://glorious-winner-q6j9wj796gr26gxx-3000.app.github.dev/api` (Used in `frontend/lib/main.dart`)

## Development Workflow
- Always update the backend API first if new data models are required.
- Maintain the Supabase schema in `backend/supabase_schema.sql`.
- Follow the **Research -> Strategy -> Execution** cycle for all new features.
