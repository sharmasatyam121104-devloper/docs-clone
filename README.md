# docs-clone

A clone of Google Docs — a real-time collaborative document editor with rich text editing, formatting, and sharing, all in the browser.

## Goal

- Rich text editor (headings, lists, bold/italic/underline, links, images, tables)
- Real-time collaboration (multiple users editing the same document simultaneously)
- Document dashboard (create, rename, delete, and search documents)
- Auto-save and version history
- Comments and suggestions
- Sharing and permissions (view, comment, edit)
- Export (PDF, DOCX) and a print-friendly view

## Tech Stack

- [Next.js](https://nextjs.org) 15.0.3 (App Router) + React 19 RC
- TypeScript 5
- Tailwind CSS 3.4 + `tailwindcss-animate`
- [shadcn/ui](https://ui.shadcn.com) components (Radix UI + CVA)
- `react-hook-form` + `zod` (forms/validation)
- `recharts` (charts), `lucide-react` (icons)

> Planned but not installed yet: Tiptap/ProseMirror for the editor, Yjs/crDB for real-time collaboration, and Prisma/Supabase for the database.

## Getting Started

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the development server |
| `npm run build` | Create a production build |
| `npm run start` | Serve the production build |
| `npm run lint` | Run ESLint |

## Project Structure

```
src/
├── app/
│   ├── layout.tsx      # Root layout (Geist fonts)
│   ├── page.tsx        # Home page (currently just a demo button)
│   └── globals.css     # Tailwind + shadcn theme variables
├── components/
│   └── ui/             # ~50 shadcn/ui components
├── hooks/
│   └── use-toast.ts    # Toast hook
└── lib/
    └── utils.ts        # cn() helper
```

## Progress — What Has Been Done So Far

**Done:**
- [x] Next.js + TypeScript project setup (create-next-app)
- [x] shadcn/ui setup — ~50 components (button, dialog, dropdown, toolbar-ready pieces, etc.)
- [x] Tailwind theme and design tokens
- [x] Basic README and project structure

**Not done yet (the actual clone has not been started):**
- [ ] Rich text editor (Tiptap/ProseMirror)
- [ ] Editor toolbar (formatting controls)
- [ ] Document dashboard (document list, create/rename/delete)
- [ ] Database and auth (document ownership)
- [ ] Auto-save
- [ ] Real-time collaboration
- [ ] Comments and sharing permissions
- [ ] Version history and export
- [ ] Tests and CI

**Status: ~5% done** — only the base UI setup is ready; nothing Google Docs-like renders yet. Next step is building the editor core.
