# incident-brief

Context pack for a live production incident on the Meridian Home account.

Read this and [`INCIDENT.md`](INCIDENT.md). Everything else you need, you will have to ask for.

## Your role

You are the senior engineer and technical lead on the Meridian Home account. You have been on
it since the start. It is Saturday morning and you are the most senior person available.

## The client

**Meridian Home** — an online homeware retailer. Around £40m of annual revenue, roughly 70% of
it through the website. Weekends carry a disproportionate share of trading.

**Priya Raman**, Head of Operations, is your day-to-day contact. She is not technical. She is
responsible to Meridian's board for anything customer-facing going wrong.

## The system

You built and run Meridian's storefront, checkout and order management. It has been live for
seven months.

- Node/TypeScript API, three instances behind a load balancer
- Managed Postgres (primary plus a read replica), roughly 2.4m orders in the table
- Card payments handled by a third-party provider; the storefront calls their hosted checkout,
  the provider calls a webhook back to confirm
- Order search and the admin console are served by the same API
- CI deploys on merge to `main`; database migrations run as a pipeline step before the new
  version is released
- Metrics and logs in Grafana; alerting to a shared channel

## The team

| | |
| --- | --- |
| **You** | Senior engineer, tech lead |
| **Tom Alderton** | Junior engineer, eight months in the industry, five on this account. Capable, keen, works weekends without being asked. Online now. |
| **Sarah Okafor** | Senior engineer, on the account but on annual leave and uncontactable until Monday |
| **Marcus Bell** | Your account director. Contactable. Not technical. |

## What happens next

Every other person in this scenario is played for you, and you will be told who is speaking
each time. Ask them anything you would ask in real life — including things you would normally
find out by looking at a dashboard or running a query. If you would check something, say so
and you will be told what you would see.

Nobody will volunteer information you do not ask for.
