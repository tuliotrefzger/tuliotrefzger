# Hi, I'm Túlio

Full-stack Software Engineer based in Brazil, building cloud-native SaaS applications with **TypeScript, AWS, PostgreSQL, NestJS, and React**.

Interested in backend, platform engineering, and full-stack roles focused on scalable cloud systems.

Currently building **Intra** — a production multi-tenant CRM and financial operations platform.

**Live Demo:** https://www.intratech.app

---

## What I'm building

### Intra — Multi-Tenant SaaS CRM & Operations Platform *(Private Repository)*

Intra is a cloud-native SaaS platform used daily by a financial-advisory company to manage:

- CRM & sales pipeline
- Client portfolios
- Operational workflows
- Advisor performance
- Revenue reporting

The platform runs on a shared AWS infrastructure while keeping customer data isolated through PostgreSQL Row-Level Security.

### My responsibilities

- Designing backend services with NestJS & Prisma
- Building React / Next.js features
- Developing AWS Lambda ETL pipelines
- Provisioning infrastructure with Terraform
- Designing database schemas and production migrations
- Improving platform architecture and developer experience

---

## Engineering highlight

One design decision I'm particularly proud of is our tenant isolation model.

Instead of relying on developers to remember adding a `WHERE tenant_id = ...` clause, PostgreSQL Row-Level Security enforces isolation automatically.

```ts
// Default client (tenant scoped)
await prisma.tenancy.task.findMany()

// Explicit privileged client
await prisma.bypassRls.company.findMany()
```

The safe path is the default.

The dangerous path is explicit.

If someone forgets tenant context, the query returns **nothing** instead of another customer's data.

---

## Other architectural decisions

- Asynchronous processing with SQS + Lambda
- Scheduled ETL pipelines isolated from request handling
- Infrastructure as Code using Terraform
- Modular monorepo architecture
- Extensive automated unit & integration testing
- Ephemeral AWS environments for feature branches

---

## Tech Stack

### Languages

TypeScript • SQL • Python • HCL

### Backend

NestJS • Prisma • PostgreSQL • Better Auth • REST APIs

### Frontend

Next.js • React • TanStack Query • Tailwind CSS • Radix UI

### Cloud

AWS • Terraform • Docker • GitHub Actions • Jenkins

### Interests

- Distributed Systems
- System Design
- Cloud Architecture
- AI Applications
- Developer Experience

---

## GitHub Stats

![Túlio's GitHub stats](https://github-readme-stats.vercel.app/api?username=tuliotrefzger&show_icons=true&hide_border=true&include_all_commits=true&count_private=true)

![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=tuliotrefzger&layout=compact&hide_border=true&langs_count=6)

---

## 📫 Let's connect

- 💼 LinkedIn: [tulio-rezende-trefzger-de-mello](https://www.linkedin.com/in/tulio-rezende-trefzger-de-mello/)
- 📧 tuliotrefzgermello@gmail.com
