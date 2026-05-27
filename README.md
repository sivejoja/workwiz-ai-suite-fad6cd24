# AI Workplace Productivity Assistant

A modern, responsive web application that helps professionals automate workplace tasks using AI.

## Features

1. **Smart Email Generator**  
   Generate professional emails with support for different tones (formal, friendly, persuasive, apologetic) and lengths (short, medium, long).

2. **Meeting Notes Summarizer**  
   Summarize long meeting notes or transcripts into structured summaries with key decisions, action items, and open questions.

3. **AI Task Planner / Scheduler**  
   Generate daily or weekly schedules by breaking goals into prioritized, actionable plans with effort estimates.

4. **AI Research Assistant**  
   Summarize topics/articles and provide structured briefings with key points, trade-offs, and next-step recommendations.

5. **AI Chatbot Interface**  
   Interactive AI workplace assistant that handles user prompts and responses for quick questions and ideation.

## Tech Stack

- **Frontend:** React, Tailwind CSS, shadcn/ui
- **Backend:** Supabase (Edge Functions)
- **AI:** Lovable AI Gateway (powered by Gemini)
- **Framework:** TanStack Start (file-based routing, server functions)

## Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── ui/             # shadcn/ui components
│   ├── app-sidebar.tsx # Sidebar navigation
│   ├── feature-shell.tsx # Feature page wrapper
│   └── ai-output.tsx   # Editable AI output component
├── routes/             # TanStack file-based routes
│   ├── __root.tsx      # Root layout (sidebar + header)
│   ├── index.tsx       # Dashboard landing page
│   ├── email.tsx       # Smart Email Generator
│   ├── meetings.tsx    # Meeting Notes Summarizer
│   ├── tasks.tsx       # AI Task Planner
│   ├── research.tsx    # AI Research Assistant
│   └── chat.tsx        # AI Chatbot Interface
├── lib/                # Utility functions & AI client
│   └── ai.ts           # AI service wrapper
├── assets/             # Images and static assets
└── styles.css          # Global styles & design tokens

supabase/
└── functions/
    └── ai-assist/      # Edge function proxying AI requests
```

## Design System

- **Theme:** Dark futuristic theme with deep violet/blue tones
- **Palette:** Primary violet (`oklch(0.72 0.18 285)`), dark backgrounds, glassmorphism cards
- **Typography:** Clean sans-serif, professional and readable
- **Layout:** Sidebar navigation + responsive main content area
- **Hero:** Futuristic 3D AI-generated hero image with gradient overlay

## Key Components

- **Sidebar Navigation:** Collapsible sidebar with icons for all tools
- **Feature Shell:** Consistent page wrapper with sticky header, icon, and Responsible AI disclaimer
- **AI Output:** Editable textarea with loading states and copy functionality
- **Dashboard Cards:** Tool overview cards linking to each feature

## Responsible AI Disclaimer

All AI-generated outputs may be inaccurate, incomplete, or biased. Users are encouraged to review and edit results before sharing or acting on them. Do not submit confidential information you wouldn't share with a third-party service.

## Getting Started

1. Install dependencies:
   ```bash
   bun install
   ```

2. Start the development server:
   ```bash
   bun dev
   ```

3. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Environment Variables

Create a `.env` file with the following:

```env
VITE_SUPABASE_URL=<your-supabase-url>
VITE_SUPABASE_PUBLISHABLE_KEY=<your-supabase-anon-key>
VITE_SUPABASE_PROJECT_ID=<your-project-id>
```

The AI Edge Function requires `LOVABLE_API_KEY` to be configured in your Supabase project settings.

## Deployment

This project is built with TanStack Start and is ready for deployment on edge platforms like Cloudflare Workers.

## License

Built by Leon Sive Joja.