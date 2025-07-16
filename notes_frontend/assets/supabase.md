# Supabase Integration for Notes Frontend

This Flutter app requires Supabase to be configured for CRUD actions on notes.
The Supabase client is initialized with the following environment variables, which must be set in your `.env` file at the project root:

- `SUPABASE_URL`: The base URL for your Supabase project.
- `SUPABASE_KEY`: The public API key (anon key) for your Supabase project.

These are read at runtime via the `flutter_dotenv` package.

**How to Configure:**
1. Create a `.env` file in the `/personal-notes-manager-ee9378b8/notes_frontend/` directory.
2. Add these lines:
   ```
   SUPABASE_URL=your_supabase_project_url
   SUPABASE_KEY=your_supabase_anon_key
   ```

**Table Required in Supabase:**
- Table name: `notes`
- Columns expected:
  - `id` (serial/int, primary key)
  - `title` (text)
  - `body` (text)
  - `created_at` (timestamp)
  - `updated_at` (timestamp)

**Usage:**
The app will auto-connect to Supabase using these values, and perform all CRUD actions on the `notes` table.
