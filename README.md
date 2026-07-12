# Wodify (wodify)

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
