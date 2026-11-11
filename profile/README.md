<p align="center">
  <img width="760" src="https://res.cloudinary.com/dbaa3pxau/image/upload/v1728625005/edust-cover_l3xkow.svg" alt="Edust — Education Management Platform">
</p>

<h1 align="center">Edust</h1>

<p align="center">
  <strong>The operating system for a learning institution.</strong><br/>
  Admissions, academics, exams, results, fees and accounting — one student record, one organisation, strict isolation.
</p>

<p align="center">
  <a href="https://www.edust.org"><img src="https://img.shields.io/badge/website-edust.org-111111" alt="Website"></a>
  <a href="https://www.edust.org/features"><img src="https://img.shields.io/badge/features-explore-2ea44f" alt="Features"></a>
  <a href="https://www.edust.org/pricing"><img src="https://img.shields.io/badge/pricing-plans-1f6feb" alt="Pricing"></a>
  <a href="https://www.edust.org/contact"><img src="https://img.shields.io/badge/contact-talk%20to%20us-8957e5" alt="Contact"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-16-000000?logo=nextdotjs&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/NestJS-11-e0234e?logo=nestjs&logoColor=white" alt="NestJS">
  <img src="https://img.shields.io/badge/Prisma-7-2d3748?logo=prisma&logoColor=white" alt="Prisma">
  <img src="https://img.shields.io/badge/PostgreSQL-16-4169e1?logo=postgresql&logoColor=white" alt="PostgreSQL">
</p>

---

## Why the name is **Edust**

**Edust** is **Educ**ation + **St**udent & **Teacher** — "edust" reads as *education* with its middle taken out and its two most important people put back in.

That is not a marketing conceit, it is the product's boundary:

- **Edu** — everything an institution must run: academic years, classes, subjects, exams, results, attendance, fees and ledgers.
- **St**udent, **St**aff, **St**ructure — the three things every record in the system is anchored to.

An institution does not fail because it lacks software. It fails because the same student exists in five places — a register, a spreadsheet, a fee book, an exam sheet and a receipt — and every one of them can disagree with the others. Edust collapses those five into **one record per student, per organisation, per academic year**, and makes every other screen a view over it.

The short version: **one student, one truth.**

---

## What Edust is

Edust is a **multi-tenant education management platform**. Each institution — called an *organisation* — gets its own isolated space: its own users, students, staff, academics, money and documents. No organisation can see another's data, and that isolation is enforced by the system rather than by convention.

It is built for how education actually runs in South Asia, not for a demo:

| Institution | What it needs | What Edust gives it |
|---|---|---|
| **School** | Class → Section → Group, yearly promotion and roll numbers | Academic-year clone, bulk promotion, result publishing |
| **Madrasah** | The same structure with different subjects and fee heads | Bangla interface, configurable subjects, flexible fee structures |
| **Coaching centre** | Batches, not classes; enrolments that start mid-year | Course & batch management with seat limits and deadlines |
| **Training centre** | Certifications and continuous education | Course delivery, materials, announcements |
| **Solo tutor** | Sell a course online, get paid | Public course page, online registration, payment-proof verification |

---

## What is inside

The platform is specified as **26 modules** across seven groups. They share one data model, so a change made in one place is visible everywhere it belongs.

<table>
<tr><td width="50%" valign="top">

**Academic core**
- Organisation, academic years & sessions
- Classes, sections and groups
- Students, guardians and enrolment
- Bulk promotion, transfer and repeat
- Subjects and curriculum mapping
- Teachers and employees

</td><td width="50%" valign="top">

**Examinations and results**
- Exam setup, subjects and routines
- Mark entry in one grid per class
- GPA, grades and positions calculated
- Results private until published, locked afterwards
- Entry passes and seat plans
- Corrections logged with a reason

</td></tr>
<tr><td valign="top">

**Fees and accounting**
- Fee categories, structures and assignments
- Monthly or termly billing runs
- Discounts, late fees and split payments
- Invoices, and a record of who collected what
- Chart of accounts, vouchers and journal entries
- Optional ledger posting — collection reports work without it
- Payroll and salary management

</td><td valign="top">

**People and access**
- Organisation members and invitations
- Role-based access control
- Personas for admin, accountant, teacher, guardian
- Attendance tracking
- Audit and logging with sensitive fields masked

</td></tr>
<tr><td valign="top">

**Courses and commerce**
- Public course pages with link previews
- Online registration and seat limits
- bKash / Nagad payment-proof submission
- Staff verification queue
- Duplicate transaction IDs detected automatically
- Class links, materials and announcements

</td><td valign="top">

**Platform**
- Reports and analytics
- Document template builder
- Subscription and package management
- Private file storage on short-lived links
- Bangla and English throughout

</td></tr>
</table>

---

## The parts most systems get wrong

**Money is not editable.** Every payment records who collected it, when, and against which invoice. A mistake is corrected by a reversal, never by quietly changing a number. That is the difference between a fee register and an audit trail.

**Results are private until you publish them.** A half-finished mark sheet never reaches a guardian. Once published, a result is locked, and any later correction carries a reason and a log entry. Guardians see only their own child's published results.

**Accounting is optional, not a wall.** Collection reports work from day one. Turn on ledger posting when the institution is ready for it, and fee collection starts posting to the chart of accounts automatically.

**Duplicate payments are caught, not reconciled later.** Two registration submissions with the same bKash transaction ID are blocked at verification, not discovered at month end.

**Every entity knows its academic year.** Cloning last year's setup produces a clean starting point with no leftover students, enrolments or payments — structure carries forward, people do not.

---

## Trust and isolation

- **Strict tenant isolation** — every record is scoped to an organisation at the data layer, not filtered in the UI.
- **Role-based permissions** — accountants, teachers and office staff get only what their job requires.
- **Private file storage** — documents and payment proofs are never publicly addressable; they are served through short-lived links.
- **Audit trail** — who did what, and when, with sensitive fields masked in the log.
- **Versioned money** — fee structures and invoices keep their history; nothing is silently rewritten.

---

## Platform status

Edust is under active development and shipping continuously. Being precise about the boundary matters more to us than a longer feature list:

- **Available today** — academic setup, students, guardians, enrolment, exams, results, attendance, fees and billing, reports, course sales with payment-proof verification, audit logging.
- **Available and opt-in** — accounting: chart of accounts, vouchers, journal entries, ledger posting.
- **On the roadmap** — automated online gateway checkout (currently bKash/Nagad proof submission with staff verification).

If a capability is not in the list above, it is not shipped yet. We would rather say that than let a feature list drift ahead of the product.

---

## Built with

A two-repo architecture: a Next.js application for the institution's interface, and a NestJS API that owns every rule, every permission check and every database transaction.

```
Next.js 16 + React + TanStack Query/Table + shadcn/ui
                        │
                        ▼
        NestJS 11 REST API, versioned and documented
                        │
                        ▼
              Prisma 7  →  PostgreSQL
```

Both sides are proprietary. This organisation publishes documentation and public materials; the application source is not open source.

---

## Documentation

| Where | What |
|---|---|
| [edust.org/features](https://www.edust.org/features) | What each module does, in plain language |
| [edust.org/pricing](https://www.edust.org/pricing) | Plans, limits and the 30-day trial |
| [edust.org](https://www.edust.org) | The platform, and the product story |

Our requirements are written as a full software requirements specification — one module document per capability, with numbered requirements, business rules, scenarios and worst-case edge cases. That specification, not a slide deck, is what the product is built against.

---

## Talk to us

- **Website** — [edust.org](https://www.edust.org)
- **Contact** — [edust.org/contact](https://www.edust.org/contact)
- **Email** — through the contact form; we answer setup and pricing questions there

If you run a school, madrasah, coaching centre or training programme and the software you use today is a folder of spreadsheets, we would like to hear what your worst week looks like. Most of our roadmap came from those conversations.

<p align="center">
  <br/>
  <sub>© 2024–2026 Edust. All rights reserved.</sub>
</p>
