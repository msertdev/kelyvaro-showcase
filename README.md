<div align="center">

# Kelyvaro

### Apply to jobs in Germany from your own e-mail — with a tailored German CV for every posting.

Profile once. Matched postings from employer career sites. An ATS-ready Lebenslauf and Anschreiben per posting.
**You approve every application; nothing is sent without you.**

[**kelyvaro.com**](https://kelyvaro.com) · Turkish & English · Germany first

</div>

<br>

<img src="./masaustu-ana.png" width="100%" alt="Kelyvaro — landing page" />

---

## What it does

Turkish job seekers — welders, electricians, truck drivers, nurses, cooks, engineers — usually pay an intermediary thousands of euros up front to reach a German employer. Kelyvaro is the tool instead of the intermediary.

| Step | What happens |
|---|---|
| **Profile** | Target country, occupation and German level open your list in under a minute; the rest is only needed for the CV. |
| **Matching** | Postings from Adzuna and employer applicant-tracking boards (Personio, SmartRecruiters, Greenhouse, Workday, Oracle, softgarden …) are scored against your profile — with the *reasons* shown, not just a number. |
| **CV & letter** | For each posting, a German tabular Lebenslauf and a DIN 5008 Anschreiben are generated. The model only writes; every fact comes from your profile and is checked against it. |
| **Sending** | The mail goes from **your own Gmail** (send-only permission). It stays in your Sent folder; the employer replies to you. |
| **Tracking** | Sent applications, replies and outcomes in one place. |

No job guarantee, no placement, no hidden fees. The first application is free; then a single monthly payment, no auto-renewal.

---

## Product

<table>
<tr>
<td width="66%"><img src="./masaustu-eslesmeler.png" alt="Matched postings with reasons and the four-step first-application guide" /></td>
<td width="34%"><img src="./mobil-eslesmeler.png" alt="Matches on mobile" /></td>
</tr>
<tr>
<td colspan="2" align="center"><sub><b>Matches.</b> Every row explains why it fits; a four-step guide walks a new user to the first free application. All traffic is mobile, so the mobile layout is the primary one.</sub></td>
</tr>
</table>

<table>
<tr>
<td width="50%"><img src="./masaustu-panel.png" alt="Dashboard with profile strength" /></td>
<td width="50%"><img src="./masaustu-cv.png" alt="CV studio" /></td>
</tr>
<tr>
<td align="center"><sub><b>Dashboard.</b> Profile strength is the only score shown — it is computed, not decorative.</sub></td>
<td align="center"><sub><b>CV studio.</b> Missing inputs are listed before anything is generated.</sub></td>
</tr>
</table>

<table>
<tr>
<td width="60%"><img src="./masaustu-rehber.png" alt="Opportunity Card points calculator" /></td>
<td width="40%"><img src="./mobil-panel.png" alt="Dashboard on mobile" /></td>
</tr>
<tr>
<td align="center"><sub><b>Guides.</b> Seven guides on German CVs, recognition (Anerkennung), the EU Blue Card and the Opportunity Card — including a points calculator built from the text of the law (§20a/§20b AufenthG).</sub></td>
<td align="center"><sub><b>Mobile dashboard.</b></sub></td>
</tr>
</table>

<img src="./masaustu-almanya.png" width="100%" alt="Occupation index for Germany with live posting counts" />
<p align="center"><sub><b>Occupation index.</b> 46 occupations with verified requirements (recognition, visa route, salary thresholds) and live posting counts.</sub></p>

---

## Under the hood

- **Next.js 15** (App Router, TypeScript strict) · **Tailwind v4** · **next-intl** (tr/en)
- **Supabase** (Postgres, RLS on every table, pg_cron) · **Vercel** (Frankfurt region)
- **Job sources:** Adzuna API, Arbeitnow, and a self-growing registry of employer ATS boards discovered from career pages — 11 providers, each verified against a live employer
- **Generation:** Groq-hosted open-weight model with structured JSON output; facts are never written by the model, only checked. Prompt regression tests with promptfoo.
- **Sending:** Gmail API with the `gmail.send` scope only; MX check before every send
- **Measurement:** GA4 + Meta CAPI + PostHog (EU), all behind explicit consent
- **Video:** launch spots rendered with Remotion from the same design tokens as the site

Design language is editorial rather than "SaaS template": Newsreader headings, Inter body, ink-and-paper palette, lines instead of cards, one accent used sparingly.

---

## Status

Live since August 2026 with paying customers on the way. Built and run by [Murat Sert](https://github.com/msertdev) with a co-founder on distribution.

Screenshots use a sample profile ("Mert Aydın"); no user data is shown.

<sub>© 2026 Kelyvaro. Screenshots and text in this repository are provided for reference only (see LICENSE).</sub>
