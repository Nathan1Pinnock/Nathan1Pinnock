## Nathan Pinnock

Co-founder and engineer at [**taskpool.ai**](https://taskpool.ai) — a live UK marketplace where agents post funded tasks and workers claim them. I work across **C# / ASP.NET Core** on the backend and **TypeScript / React / Astro** on the frontend, and I run the infrastructure it ships on.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Nathan_Pinnock-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nathan-pinnock-3683a0260/)

*Open to graduate and junior software engineering roles.*

---

### TaskPool &nbsp;·&nbsp; [taskpool.ai](https://taskpool.ai)

I co-founded TaskPool and write a large share of its code — **390 commits** into a 1,100+ commit codebase, alongside two co-founders and a non-executive director. It handles real payments, real users and a live threat model. The source is private, so here is what I actually build:

**Backend — ASP.NET Core 10, C#**
- Strict **Clean Architecture** with a one-way dependency rule: `Api → Infrastructure → Application → Domain`. The Domain project has *zero* package and project references, so business rules stay independent of EF Core, ASP.NET and every third-party SDK.
- **Transactional outbox pattern** for reliable event dispatch — domain events commit in the same transaction as the state change, then a hosted background poller delivers them, so a crash mid-publish cannot lose or duplicate an event.
- **JWT auth with refresh-token rotation**, plus a background purge service for expired tokens.
- **Stripe Connect Express** for marketplace payouts.

**Frontend — Astro + React islands, TypeScript**
- Static-first build with React only where interactivity is genuinely needed, keeping JavaScript off the pages that do not need it.
- A shared design system consumed across the site.

**Infrastructure and quality**
- **Docker** with separate dev and production Compose stacks, `docker-bake` builds, and nginx serving the static frontend behind hardened headers.
- **Playwright** end-to-end suite against a deployed environment, plus unit and integration test projects.
- Merge-request review on every change, with periodic **security and QA sweeps** written up against a documented threat model.
- An **architecture decision register** — choices like "hosted poller rather than Hangfire" are recorded with their trade-offs and cited by ID from the code that implements them.

> Building this taught me the things tutorials skip: how to stop a layered codebase rotting, why "just add a background job" is really a distributed-systems decision, and how to review someone else's merge request properly.

---

### Homelab and self-hosting

Most of what I know about Linux and networking I learned by running things at home rather than reading about them:

- **Jellyfin media server** — self-hosted, administered and maintained by me.
- **Raspberry Pi home automation** — scripting and scheduling jobs that run unattended around the house.
- **Personal storage and backups** — provisioning, sharing and keeping the data intact.

Running your own services teaches you what happens when they break at 1am, which turns out to be the useful half.

---

### Tech

**Languages** &nbsp;C# · TypeScript · JavaScript · Python · SQL · x86-64 Assembly

**Backend** &nbsp;ASP.NET Core · Entity Framework Core · REST APIs · SQL

**Frontend** &nbsp;React · Astro · HTML · CSS

**Infrastructure** &nbsp;Docker · Docker Compose · nginx · Linux · Git · GitLab CI · Playwright

---

### Other projects

| Project | What it is |
|---|---|
| [**Assemblyhook**](https://github.com/Nathan1Pinnock/Assemblyhook) | An HTTP client in **x86-64 assembly** — raw Linux syscalls, manual TCP socket setup, hand-built HTTP framing. No libc. |
| [**M-M-Clicker**](https://nathan1pinnock.github.io/M-M-Clicker/) | Incremental clicker game in vanilla JS with `localStorage` saves. **[Play it →](https://nathan1pinnock.github.io/M-M-Clicker/)** |
| [**chessss2**](https://github.com/Nathan1Pinnock/chessss2) | Python chess engine using minimax with alpha-beta pruning. |
| [**ToDoList**](https://github.com/Nathan1Pinnock/ToDoList) · [**BudgetApp**](https://github.com/Nathan1Pinnock/BudgetApp) | Small Tkinter desktop apps — early work, kept because everyone starts somewhere. |

---

### Contact

**LinkedIn** — [nathan-pinnock](https://www.linkedin.com/in/nathan-pinnock-3683a0260/) &nbsp;·&nbsp; **Email** — nathan1pinnock@gmail.com
