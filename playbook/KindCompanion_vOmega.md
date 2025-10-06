# KINDCOMPANION PLAYBOOK â€” VERSION Î© (FINAL ANCHOR)

**Baseline Locked:** 2025-10-06 13:00 BST  
**Entity:** KindCompanion AI Ltd (UK)  
**ICO Registration:** ZB992047 (valid to 17 Sept 2026)  
**Mission:** Privacy-first AI companion delivering empathetic, compliant, multilingual and voice-enabled support worldwide.  
**Motto:** Kindness | Companionship | Compliance.

---

## I. COMPANY OVERVIEW
- Privacy-first; no-storage-by-default.
- Global availability (multilingual) with voice.
- Channels: WhatsApp primary; landing on Netlify; payments via Stripe.

---

## II. TECH STACK ARCHITECTURE
| Layer | Platform | Purpose | Notes |
|---|---|---|---|
| Hosting & DNS | Netlify (kindcompanionchat) | Landing site, SSL, CDN | Netlify DNS (NS1â€“4) |
| Cloud Backbone | Google Cloud Platform (kindcompanion-prod) | Core compute, APIs | Secret Manager + Workload Identity Federation |
| Automation | Make.com | Workflow orchestration | Stripe â†” WhatsApp â†” GCP â†” Zoho â†” Monitoring |
| Messaging | WhatsApp Cloud API (Meta) | Primary chat channel | Dedicated number + permanent token |
| Payments | Stripe | Â£1 / week & Â£4 / month tiers | Webhooks â†’ Make.com |
| Email | Zoho Mail | support@, simon@ | Filters + auto-replies |
| Source Control | GitHub | CI/CD + Issues | 2FA ON |
| Monitoring | UptimeRobot | Site/API uptime | Hourly ping via Make |
| Device | HP OmniBook 7 AI (Windows 11) | Primary dev ops | BitLocker + password vault |
| AI Engine | OpenAI (GPT-5) | Core reasoning | API key in Secret Manager |

**Future-Ready Slots (inactive vÎ©):** Cloudflare (security), Firebase (push), Vercel (tests).

---

## III. DATA & SECURITY STACK
- **Secret Management:** GCP Secret Manager (scoped per service).
- **Identity Federation:** WIF between Make.com and GCP (no static keys).
- **Storage Policy:** No-storage-by-default; ephemeral runtime memory only. MemoryVault is user-opt-in, encrypted.
- **Encryption:** TLS 1.3 in transit, AES-256 at rest (GCP-managed).
- **CI/CD:** GitHub Actions â†’ Netlify deploy â†’ Make.com health check.
- **Backups:** Git tags, Netlify deploy snapshots, periodic GCP export.
- **Zero Trust:** Least privilege, dedicated service accounts, restricted egress.

---

## IV. COMPLIANCE STACK
| Framework | Status | Scope |
|---|---|---|
| UK GDPR / EU GDPR | âœ… | Data processing, consent, rights |
| EU AI Act (2025) | âœ… | Risk tier: Limited-Risk Companion |
| ICO Registration | âœ… ZB992047 | UK Data Controller |
| DSR (Access/Erase) Portal | Planned | /privacy/dsr (Make + Zoho) |
| DPIA | vÎ© complete | Stored /compliance/dpia_vOmega.pdf (to be created) |
| Policies | âœ… | Privacy, Cookie, ToS published on site |

**Principles:** Privacy-by-design, human-in-the-loop escalation, transparency log, model/version notice.

---

## V. TRUST & SAFETY
- **ConsentClockâ„¢:** Prominent consent indicator + one-tap revoke.
- **MemoryVault:** Optional encrypted journal; retention duration visible; export+delete self-service.
- **RealityCheck:** Periodic reminders of AI nature, limits, and safety guidance.
- **BoundaryEngine:** Guardrails for romance, finance, medical, legal; crisis routing guidance.
- **StressMonitor:** Lexical/semantic distress detection â†’ gentle de-escalation + resources.

---

## VI. PRODUCT STACK
| Module | Status | Channel | Notes |
|---|---|---|---|
| Core Chat | âœ… Live | WhatsApp | Â£1/Â£4 subscription gates |
| Relationship Mode | âœ… Alpha | WhatsApp | Empathy-focused prompts |
| Voice Companion | ðŸŸ¢ ON | Speech I/O | Whisper STT + TTS roadmap |
| Global Multilingual | ðŸŸ¢ ON | Auto-detect | Top-100 languages |
| Landing Page | âœ… | Netlify | CTA â†’ wa.me/447353685036 |
| Payments | âœ… | Stripe | Live payment links |
| Analytics | âš™ï¸ Planned | Plausible | Privacy-friendly |
| Referrals | âš™ï¸ Phase 2 | Make.com | Incentive loop |

---

## VII. EVAL & QA
**KPIs:** Empathy score, Consent accuracy, Boundary integrity, Latency, CSAT.  
**Cadence:** Hourly uptime ping; Daily self-audit (Make); Weekly manual QA; Monthly DPIA spot-check.

---

## VIII. MONETISATION
| Tier | Price | Channel | Benefits |
|---|---|---|---|
| Weekly | Â£1 | WhatsApp | Unlimited messages |
| Monthly | Â£4 | WhatsApp | Bonus voice sessions |

**LTV Goal:** Â£48/year â€¢ **CAC Target:** â‰¤ Â£5 â€¢ **Gross Margin:** > 90%  
**Upsell:** Premium Voice, Couples Mode, B2B API.

---

## IX. MARKETING & GROWTH
- Landing: Netlify (SEO, FAQs, transparent policies).
- Channels: WhatsApp CTA, Zoho email, organic SEO, founder updates.
- A/B tests: headline, CTA wording, price framing.
- Referrals: Make.com scenario, auto-track via Stripe metadata.
- Analytics: Plausible (no cookies by default, EU hosting).
- PR: Thought leadership on AI empathy & privacy.

---

## X. OPS & GOVERNANCE
- ChairOps cadence: Daily micro-audit; Weekly macro-review.
- Reporting: /reports (Finance, Compliance, Growth).
- Incident Response: 24h SLA via Zoho + WhatsApp.
- Change Control: PR-based workflow; review gates.
- Audit Trail: Make logs + Git commits.

---

## XI. ACTION BOARD (TOP 10)
1) Publish Playbook vÎ© to /docs repo.
2) Deploy updated landing (Netlify) with SEO + CTA.
3) Enable Plausible Analytics.
4) Configure Make.com daily self-audit scenario.
5) Launch Voice Companion (Whisper+TTS beta).
6) Localise prompts (Top 10 languages).
7) Draft DSR portal (access/delete).
8) Run CTA A/B tests.
9) Design referral incentive flow.
10) Create weekly ChairOps audit template.

---
**End vÎ©**