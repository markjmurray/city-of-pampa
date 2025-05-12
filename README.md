# city-of-pampa

# LocalGov.ai

**LocalGov.ai** is an AI-powered assistant for city websites that helps citizens quickly find and understand local services like trash pickup, zoning rules, permits, and more. Built with V0.dev and Supabase, this system modernizes the experience of navigating municipal resources.

---

## 🧠 Features
- Conversational chatbot trained on local ordinances and service data
- Search zoning, permit forms, trash schedules, and more
- Easy-to-use frontend UI built in V0.dev
- Backend GPT API route with Supabase integration

---

## 🛠️ Tech Stack
- Frontend: [V0.dev](https://v0.dev), React, Tailwind
- Backend: Supabase (PostgreSQL, pgvector), OpenAI (GPT-4)
- Hosting: Vercel or Supabase Edge Functions

---

## 🚀 How to Use

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/localgov-ai.git
cd localgov-ai
```

### 2. Set Up Environment
Create a `.env.local` file:
```bash
OPENAI_API_KEY=your_openai_key
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_anon_or_service_key
```

### 3. Install Dependencies
```bash
npm install
```

### 4. Run the App
```bash
npm run dev
```

### 5. Deploy to Vercel
[Deploy with Vercel](https://vercel.com/import)

---

## 🗃 Supabase Tables
Ensure the following tables exist:

### `city_services`
```sql
create table city_services (
  id uuid primary key default gen_random_uuid(),
  name text not null,
  description text,
  contact_info text,
  service_area text,
  meta jsonb
);
```

### `permit_forms`
```sql
create table permit_forms (
  id uuid primary key default gen_random_uuid(),
  name text not null,
  description text,
  file_url text,
  requirements text,
  category text,
  updated_at timestamp default now()
);
```

---

## 📬 Contact
Have questions or want to use this in your city? Reach out to the [Humanity AI team](https://getthelab.com).

---

Built with ❤️ by Humanity AI
