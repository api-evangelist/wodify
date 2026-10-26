# Wodify (wodify)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Wodify is gym, fitness, and CrossFit box management software covering membership management, billing, class scheduling, lead and client CRM, digital waivers, and workout/performance tracking.

## API Access Model (Honest Summary)

Wodify publishes a **documented public REST API** at `https://api.wodify.com/v1`. Access is real but **gated by an API key**:

- **Authentication:** every request carries an `x-api-key` header. There is no public, unauthenticated data plane.
- **Getting a key:** customers on the **Wodify Workflows** feature already have a key (Wodify Core > Digital Presence > Web Integrations > API Keys). **Partners** request a key through the **Wodify Developer Portal**.
- **Docs:** the reference (`https://docs.wodify.com`) is public to read, and Wodify publishes a machine-readable operation index at `https://docs.wodify.com/llms.txt`.
- **What was verified:** the base URL, the `x-api-key` auth, and the paths and query parameters for the core collections (`/v1/clients`, `/v1/classes`, `/v1/workouts`, `/v1/programs`, `/v1/services`) were confirmed directly against the live reference. The remaining collections in this entry are modeled from Wodify's public, consistently named REST operation catalog and are **not fabricated** - but the exact path strings and payload schemas for those should be confirmed against the live docs during reconciliation.
- **Transport:** REST over HTTPS only. **No documented public WebSocket API** (see `review.yml`).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/wodify/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/wodify/refs/heads/main/apis.yml)

## Tags

- Fitness
- Gym Management
- Membership Management
- Fitness Software
- CrossFit
- Class Scheduling
- Billing
- Wellness
- SaaS

## Timestamps

- **Created:** 2026-07-12
- **Modified:** 2026-07-12

## APIs

### Wodify Clients API

Create, retrieve, update, search, suspend, reinstate, deactivate, and reactivate gym clients (members), plus manage client tags, groups, roles, statuses, waivers, and registration links.

- **Human URL:** [https://docs.wodify.com/reference/get_clients](https://docs.wodify.com/reference/get_clients)
- **Base URL:** `https://api.wodify.com/v1`

### Wodify Leads API

Manage prospective members - create, get, update, delete, and search leads, convert leads to clients, and work with lead sources, statuses, tags, groups, bookings, reservations, and sign-ins.

- **Human URL:** [https://docs.wodify.com/reference/get_leads-1](https://docs.wodify.com/reference/get_leads-1)
- **Base URL:** `https://api.wodify.com/v1`

### Wodify Memberships API

Create, edit, delete, search, and deactivate memberships and membership templates; manage auto-renew, holds and hold reasons, discounts, accessible locations and programs, attendance types, billing days, and payment plan templates.

- **Human URL:** [https://docs.wodify.com/reference/get_memberships-1](https://docs.wodify.com/reference/get_memberships-1)
- **Base URL:** `https://api.wodify.com/v1`

### Wodify Classes and Programs API

Retrieve and search classes and programs, read waitlists, and manage class reservations, sign-ins, and drop-in reservations for clients, leads, and drop-ins.

- **Human URL:** [https://docs.wodify.com/reference/get_classes-1](https://docs.wodify.com/reference/get_classes-1)
- **Base URL:** `https://api.wodify.com/v1`

### Wodify Workouts and Performance API

Create, retrieve, update, delete, and search workouts (WODs), and manage skill progressions, levels, criteria, and per-client progression enrollment and promotion.

- **Human URL:** [https://docs.wodify.com/reference/get_workouts-1](https://docs.wodify.com/reference/get_workouts-1)
- **Base URL:** `https://api.wodify.com/v1`

### Wodify Services and Appointments API

Retrieve and search appointment services, and manage client and lead appointment bookings.

- **Human URL:** [https://docs.wodify.com/reference/get_services-1](https://docs.wodify.com/reference/get_services-1)
- **Base URL:** `https://api.wodify.com/v1`

### Wodify Financials API

Read invoices, transactions, and payment methods, and manage discounts, tax rates, revenue categories, contract templates, and Stripe options for gym billing.

- **Human URL:** [https://docs.wodify.com/reference/get_invoices](https://docs.wodify.com/reference/get_invoices)
- **Base URL:** `https://api.wodify.com/v1`

### Wodify Communications API

Send email, SMS, and in-app chat to clients, leads, drop-ins, and segments; manage tasks, task followers and people, email templates, media library assets, and group phone numbers.

- **Human URL:** [https://docs.wodify.com/reference/send_email-1](https://docs.wodify.com/reference/send_email-1)
- **Base URL:** `https://api.wodify.com/v1`

## Common Properties

- [Domain Security](security/wodify-domain-security.yml)
- [Authentication](authentication/wodify-authentication.yml)
- [LinkedIn](https://www.linkedin.com/company/wodify)
- [Website](https://www.wodify.com)
- [Documentation](https://docs.wodify.com)
- [Plans](plans/wodify-plans-pricing.yml)
- [Rate Limits](rate-limits/wodify-rate-limits.yml)
- [Fin Ops](finops/wodify-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
