# Security Policy — GitHat Inc

## Reporting a vulnerability

Email **security@githat.io** with:
- Description of the vulnerability + affected component (githat.io / api.githat.io / SDKs / consumer apps)
- Reproduction steps or proof-of-concept
- Your name + handle if you want public credit

We acknowledge within 48 hours, scope within 5 business days, and patch within 90 days for non-critical (faster for critical).

## Scope

In scope:
- githat.io marketing + dashboard
- api.githat.io (Lambda backend in `GitHat-IO/MicroBackEnds`)
- @githat/nextjs SDK
- create-githat-app CLI
- Any GitHat-platform consumer app you suspect a cross-tenant boundary issue on

Out of scope:
- Third-party services (AWS, Stripe, SES, GitHub)
- Social-engineering attacks against employees
- Denial-of-service / volumetric attacks (covered by AWS Shield Standard)
- Issues in consumer apps unrelated to GitHat auth

## Cryptography + identity

- JWT signing: RS256 via AWS KMS (no shared signing secret with consumers)
- Public verification material: JWKS at `https://api.githat.io/.well-known/jwks.json`
- Audience-claim enforcement per consumer app
- CAA records on every platform domain (lockdown: amazon.com + amazon trust)

## Preferred languages

English.
