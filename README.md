# pub.dev

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
