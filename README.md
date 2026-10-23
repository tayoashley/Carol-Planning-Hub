# Carol Planning Hub

Single-page app (index.html, no build step) plus four brand images. Files must stay in the same folder.

Runs as a Claude Artifact using two Claude runtime capabilities:
- db: shared data (collections: members, tasks, settings, chat; tasks/{id}/comments)
- sample: the "Ask the planner" assistant

Outside Claude these capabilities do not exist, so the page will load but cannot read or save data. To self-host, replace the `claude.use('db')` and `claude.use('sample')` calls with your own backend (for example Firebase/Supabase and an LLM API behind a server).

Data model, seeded starter tasks and members are not included here (PINs are not stored in code).
Sign-in is client-side (name + SHA-256 hashed PIN): light security only.
