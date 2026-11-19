<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f766e,100:065f46&height=190&section=header&text=Athanasius%20Adaawon%20Ataarem&fontSize=36&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=IT%20Specialist%20%C2%B7%20Full-Stack%20Developer%20%C2%B7%20Ghana&descSize=17&descAlignY=57" alt="banner" />

<a href="https://github.com/athanasius-ataarem">
<img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=500&size=20&duration=3500&pause=900&color=10B981&center=true&vCenter=true&width=680&lines=I+build+and+operate+production+systems+end+to+end;TypeScript+%C2%B7+Node+%C2%B7+React+%C2%B7+PostgreSQL;Payments%2C+SMS+%26+offline-first+apps+for+Ghana" alt="typing intro" />
</a>

<img width="100%" src="https://raw.githubusercontent.com/athanasius-ataarem/athanasius-ataarem/main/assets/at-a-glance.svg" alt="Engineering at a glance: 5 production systems, 2,300+ automated tests, 1,900+ commits since June 2026, 83% TypeScript" />

I design, build, and **operate** production systems end to end, from the database
schema to the server they run on.

At [NABOCADO](https://nabocado.org.gh), a development organisation in northern Ghana, I built
and run the organisation's software on my own: a fleet-management system, a single sign-on
service, a leave portal and an IT helpdesk. Through **Athan Digital** I build systems for
clients, including a guest-lodge booking system with mobile-money payments.

🎬 **Start here → [Portfolio](https://github.com/athanasius-ataarem/portfolio)**: screenshots,
narrated demos and engineering notes.<br/>
The production code is in private repositories because it belongs to my employer and my
clients. **I'm happy to walk through it on a call.**

</div>

---

## 🏗️ Production systems

| System | What it does | Built with |
| --- | --- | --- |
| **🚐 NABOCADO Transport**<br/><sub>[fleet.nabocado.org.gh](https://fleet.nabocado.org.gh) · live since Oct 2026</sub> | Fleet management. Drivers log trips and fuel on their phones **offline** and the app syncs when a signal returns. Odometer-gap and fuel-efficiency checks, vehicle costs split across donor projects by kilometre, verified records made immutable by PostgreSQL triggers, and no location data collected, by design (Data Protection Act, 2012). | TypeScript, Express, Prisma, PostgreSQL, React PWA with an IndexedDB outbox; **1,145 tests**; CI-gated deploys |
| **🔐 NABOCADO ID** | Single sign-on for the organisation's apps: short-lived RS256-signed JWTs checked for audience, replay and state, a staff directory API for apps with service tokens, and two-step sign-in (TOTP). | TypeScript, Express, jose, Argon2, PostgreSQL; **237 tests** |
| **🏨 Restall Guest Lodge**<br/><sub>[restallguestlodge.com](https://restallguestlodge.com) · client project, Athan Digital</sub> | Booking website, staff app and API. Paystack deposits by **mobile money and card**, with refunds; webhooks verified by HMAC signature and idempotent. SMS through Arkesel and Hubtel and WhatsApp messages through a provider queue that retries. Live updates over WebSockets. | Fastify, Drizzle, PostgreSQL, React PWA, Astro; **Docker** on Hetzner; Cloudflare Pages and R2 |
| **🌿 NABOCADO Leave Portal**<br/><sub>[leave.nabocado.org.gh](https://leave.nabocado.org.gh) · live since Jul 2026</sub> | Paper leave forms turned into a digital workflow: routed approvals with digital signatures, an append-only balance ledger enforced by database triggers, an email outbox with retries, and print-perfect A4 PDFs. | Express, Prisma, PostgreSQL, React; **288 tests**; 25 ADRs |
| **🛠️ NABOCADO IT Helpdesk**<br/><sub>[helpdesk.nabocado.org.gh](https://helpdesk.nabocado.org.gh) · live since Jun 2026</sub> | Ticketing app staff install on their phones: an office-hours SLA clock, reply by email, an equipment register, push notifications and monthly PDF reports. | Fastify, Drizzle, SQLite, React PWA |
| **🏫 SchoolOS**<br/><sub>own product · on staging, ready for its first school</sub> | Multi-tenant school management for Ghanaian private schools: report cards, fees, Paystack payments split to each school, and SMS sign-in codes. Works offline on low-end Android phones. | Express, PostgreSQL **row-level security**, React PWA, Docker; Playwright offline end-to-end tests; **711 integration tests** |
| **🌐 nabocado.org.gh**<br/><sub>rebuilt Oct–Nov 2026</sub> | The organisation's public website, now under version control with a staging copy, GitHub Actions deploys and Cloudflare in front. | Laravel 13, Filament, MySQL |

## 🔓 Public code

| Repository | |
| --- | --- |
| [**leave-portal-docs-chat**](https://github.com/athanasius-ataarem/leave-portal-docs-chat) | RAG and tool-calling demo: Claude answers questions about the Leave Portal docs and cites what it used, with cost control and abuse resistance built in. |
| [**daybook**](https://github.com/athanasius-ataarem/daybook) | Offline-first daily cashbook for single-shop traders: cash and mobile money in and out, close-of-day reconciliation, and a WhatsApp summary. TypeScript PWA with Prisma and PostgreSQL. |
| [**portfolio**](https://github.com/athanasius-ataarem/portfolio) | Screenshots, narrated demos and engineering notes for the Leave Portal and the Helpdesk. |

## ⚙️ How I work

- **The database enforces the rules.** Append-only ledgers, triggers and constraints, so a bug in the app can't quietly rewrite history.
- **CI gates releases.** Type checks, lint, tests against a real PostgreSQL and a dependency audit run on every push; on the fleet and sign-on systems only a passing commit can be deployed.
- **Built for real networks.** Offline-first apps for Android phones, sync that is safe to repeat, and retries for SMS, email and webhooks.
- **Operated, not just shipped.** Runbooks, nightly off-site backups with restore drills, and monitoring that alerts only when something is wrong.
- **AI-assisted, verified.** I use Claude as a coding agent, approve every change to a live system, and record significant decisions as ADRs.

## 🧰 Tech stack

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?style=for-the-badge&logo=fastify&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle-C5F74F?style=for-the-badge&logo=drizzle&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logoColor=white)

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux_Ops-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![nginx](https://img.shields.io/badge/nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Microsoft Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)

![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![Paystack](https://img.shields.io/badge/Paystack-00C3F7?style=for-the-badge&logoColor=white)

</div>

## 📊 GitHub activity

<div align="center">

<img height="165" src="https://raw.githubusercontent.com/athanasius-ataarem/athanasius-ataarem/main/assets/languages.svg" alt="Languages across all projects including private" />

*Most of my work is in private production repositories, which is what the
contribution graph shows. Code walkthroughs are available on request.*

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/athanasius-ataarem/athanasius-ataarem/output/github-snake.svg" />
  <img width="92%" src="https://raw.githubusercontent.com/athanasius-ataarem/athanasius-ataarem/output/github-snake-light.svg" alt="contribution snake" />
</picture>

</div>

## 📫 Get in touch

<div align="center">

[![Email](https://img.shields.io/badge/ataarem%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ataarem@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ataarem-athanasius)

<img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=dark" alt="dev quote" />

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:065f46,100:0f766e&height=100&section=footer" alt="footer" />

</div>
