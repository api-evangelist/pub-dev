# pub.dev

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

pub.dev is the official package repository for Dart and Flutter apps, supported by Google. It provides a public REST API for searching packages, retrieving package metadata and version history, downloading package archives, and accessing publisher and scoring information.

## API

The pub.dev API is free, public, and requires no authentication. All documented endpoints are available at `https://pub.dev/api`.

### Documented Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/package-name-completion-data` | Top package names for autocomplete (cache 8h min) |
| GET | `/api/package-names` | All package names with pagination (cache 2h min) |
| GET | `/api/packages/{package}` | Package metadata and full version history |
| GET | `/api/packages/{package}/versions/{version}` | Specific version metadata |
| GET | `/api/packages/{package}/publisher` | Publisher information (cache 2m min) |
| GET | `/api/packages/{package}/score` | Scoring metrics and tags (cache 2m min) |
| GET | `/api/search?q={query}` | Search packages by keyword, platform, SDK, topic |
| GET | `/feed.atom` | RSS/Atom feed of new packages |

### Caching

Consumers are expected to honor minimum cache durations to reduce load on pub.dev servers:

- Package name completion data: 8-hour minimum
- Full package name listing: 2-hour minimum
- Publisher/score endpoints: 2-minute minimum

## Resources

- **API Documentation**: https://pub.dev/help/api
- **Help**: https://pub.dev/help
- **Source Code**: https://github.com/dart-lang/pub-dev
- **Terms of Service**: https://developers.google.com/terms/
- **Privacy Policy**: https://www.google.com/intl/en/policies/privacy/
- **Security**: https://pub.dev/security
- **Contact**: support@pub.dev
- **Feed**: https://pub.dev/feed.atom

## Plans

The API is completely free with no paid tiers. See [plans/plans.yml](plans/plans.yml) for details.

## Rate Limits

No explicit rate limits are documented. See [rate-limits/rate-limits.yml](rate-limits/rate-limits.yml) for caching requirements and recommendations.

## FinOps

Zero cost. See [finops/finops.yml](finops/finops.yml) for details.
