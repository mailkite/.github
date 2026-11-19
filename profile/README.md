<p align="center">
  <img src="https://raw.githubusercontent.com/mailkite/server/main/brand-assets/logo-email.png" width="72" alt="MailKite">
</p>

# MailKite

**Receive email as a webhook. Send with one API.**
Email infrastructure for developers shipping multiple products — and the agents they build.

[Website](https://mailkite.dev) · [Docs](https://mailkite.dev/docs) · [Hosted MCP](https://mcp.mailkite.dev) · [Community](https://github.com/mailkite/community/discussions)

Every repo here works without a MailKite account. The hosted version is one way to run it, not a dependency.

---

## Start here

### [`server`](https://github.com/mailkite/server) — run the mail server yourself

Haraka SMTP (MX + submission) and an IMAP head wrapped around one small HTTP backend
contract. Self-hosted, AGPL-3.0, no vendor in the path.

```sh
git clone https://github.com/mailkite/server && cd server
cp .env.example .env          # set HMAC_SECRET
docker compose up -d          # backend + web console on :8787
```

### [`mail-parse`](https://github.com/mailkite/mail-parse) — a streaming MIME parser

Streaming, memory-efficient and fully typed, with a declarative middleware seam — for when
`postal-mime` or `mailparser` is the wrong shape for the job. Go and Python ports
([`mail-parse-go`](https://github.com/mailkite/mail-parse-go),
[`mail-parse-py`](https://github.com/mailkite/mail-parse-py)) produce the same
failure signature, so a parse failure reproduces across languages.

### [`agent-skills`](https://github.com/mailkite/agent-skills) — email for coding agents

`npx skills add mailkite/agent-skills`. Receive as a webhook, send over a verified domain,
give an agent its own inbox.

## SDKs

| | Package | Repo |
|---|---|---|
| Node | `mailkite` (npm) | [`mailkite-node`](https://github.com/mailkite/mailkite-node) |
| Python | `mailkite-dev` (PyPI) | [`mailkite-python`](https://github.com/mailkite/mailkite-python) |
| PHP | Packagist | [`mailkite-php`](https://github.com/mailkite/mailkite-php) |
| Ruby | `mailkite` (RubyGems) | [`mailkite-ruby`](https://github.com/mailkite/mailkite-ruby) |
| Go | — | [`mailkite-go`](https://github.com/mailkite/mailkite-go) |
| Java | `dev.mailkite:mailkite` | [`mailkite-java`](https://github.com/mailkite/mailkite-java) |
| .NET | — | [`mailkite-dotnet`](https://github.com/mailkite/mailkite-dotnet) |
| Elixir | — | [`mailkite-elixir`](https://github.com/mailkite/mailkite-elixir) |
| Rust | — | [`mailkite-rust`](https://github.com/mailkite/mailkite-rust) |
| Kotlin / Android | `dev.mailkite:mailkite-client` | [`mailkite-kotlin`](https://github.com/mailkite/mailkite-kotlin) |
| Swift | `MailKiteClient` (SwiftPM) | [`mailkite-swift`](https://github.com/mailkite/mailkite-swift) |
| Flutter | `mailkite_client` | [`mailkite-flutter`](https://github.com/mailkite/mailkite-flutter) |
| Expo | `@mailkite/expo` | [`mailkite-expo`](https://github.com/mailkite/mailkite-expo) |
| JS / browser | `@mailkite/client` | [`mailkite-js`](https://github.com/mailkite/mailkite-js) |
| MCP | `@mailkite/mcp` | [`mailkite-mcp`](https://github.com/mailkite/mailkite-mcp) |
| CLI | `@mailkite/cli` | [`mailkite-cli`](https://github.com/mailkite/mailkite-cli) |

SDK repos are read-only mirrors of the monorepo — open issues here, not there.

## Integrations

| Framework / tool | Repo |
|---|---|
| Next.js | [`next-mailkite`](https://github.com/mailkite/next-mailkite) · [`mailkite-nextjs-inbox`](https://github.com/mailkite/mailkite-nextjs-inbox) |
| Nuxt | [`nuxt`](https://github.com/mailkite/nuxt) · [`nuxt-mailkite`](https://github.com/mailkite/nuxt-mailkite) |
| Astro | [`astro`](https://github.com/mailkite/astro) · [`astro-mailkite`](https://github.com/mailkite/astro-mailkite) |
| Laravel | [`laravel`](https://github.com/mailkite/laravel) · [`forge`](https://github.com/mailkite/forge) · [`ploi`](https://github.com/mailkite/ploi) · [`runcloud`](https://github.com/mailkite/runcloud) |
| Symfony | [`symfony-mailer`](https://github.com/mailkite/symfony-mailer) |
| Better Auth | [`mailkite-better-auth`](https://github.com/mailkite/mailkite-better-auth) · [`mailkite-better-auth-inbox`](https://github.com/mailkite/mailkite-better-auth-inbox) |
| Supabase | [`supabase-mailkite`](https://github.com/mailkite/supabase-mailkite) |
| Spring Boot | [`spring-boot-starter`](https://github.com/mailkite/spring-boot-starter) |
| ASP.NET Core | [`aspnet-core`](https://github.com/mailkite/aspnet-core) |
| Nodemailer | [`nodemailer-mailkite-transport`](https://github.com/mailkite/nodemailer-mailkite-transport) |
| n8n | [`n8n-nodes-mailkite`](https://github.com/mailkite/n8n-nodes-mailkite) |
| Zapier | [`zapier-mailkite`](https://github.com/mailkite/zapier-mailkite) |
| Pipedream | [`pipedream`](https://github.com/mailkite/pipedream) |
| GitHub Actions | [`send-email-action`](https://github.com/mailkite/send-email-action) |
| Claude Code | [`claude-code`](https://github.com/mailkite/claude-code) |
| WordPress | [`mailkite-smtp`](https://github.com/mailkite/mailkite-smtp) · [`mailkite-mailboxes`](https://github.com/mailkite/mailkite-mailboxes) |

## Starters

[`saas-startup`](https://github.com/mailkite/saas-startup) ·
[`mailkite-examples`](https://github.com/mailkite/mailkite-examples) (30+ stacks) ·
[`mailkite-inbound-inbox`](https://github.com/mailkite/mailkite-inbound-inbox) ·
[`flask-starter`](https://github.com/mailkite/flask-starter) ·
[`fastapi-starter`](https://github.com/mailkite/fastapi-starter) ·
[`nestjs-starter`](https://github.com/mailkite/nestjs-starter) ·
[`better-auth-demo`](https://github.com/mailkite/better-auth-demo)

## What the `demo-*` repos are

One repo per provider we are compared with — Resend, SendGrid, Mailgun, Postmark, SES,
Cloudflare Email Routing, Gmail API, Microsoft Graph and more. Each one runs MailKite's
receive → verify → think → reply loop next to a runnable version of that provider's inbound
path, so you can diff them yourself instead of taking a comparison page's word for it.
They are reference code, not products.

## Notes

- **`server` is AGPL-3.0.** The MailKite name and logo are trademarks; forks must use their
  own name and branding.
- Questions and ideas go to [`community`](https://github.com/mailkite/community/discussions).
- Pre-1.0 everywhere. Where something is unproven, the README says so.
