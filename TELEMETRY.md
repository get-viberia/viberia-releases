# Viberia Telemetry

Viberia sends two telemetry pings on each app launch.

## 1) `dau_app_open` (consent-gated)

Purpose: DAU and per-install retention.

- Sent only when `analytics_enabled` is on (`Settings -> Privacy & Analytics`)
- Transport: PostHog SDK (existing US project)
- Identifier: `installation_id` (same value as `telemetry_distinct_id`)

Payload properties:

- `installation_id`
- `app_version`
- `platform` (`macos | windows | linux | unknown`)
- `first_seen_at_ms`
- `ping_schema_version`

## 2) `cohort_app_open` (anonymous cohort retention)

Purpose: population-level cohort and retention analysis.

- Sent by default on each app open for non-suppressed locales, regardless of `analytics_enabled`
- Fully suppressed for German/Austrian detection:
  - locale starts with `de-DE` or `de-AT`, or
  - timezone is `Europe/Berlin` or `Europe/Vienna`
- User-facing opt-out available in `Settings -> Privacy & Analytics` via
  `Anonymous cohort retention pings`
- Transport: direct HTTPS to PostHog Cloud-EU `https://eu.i.posthog.com/i/v0/e/`
- No per-user identifier in payload

Payload properties (only):

- `install_iso_month`
- `current_iso_week`
- `days_since_install_bucket`
- `days_since_last_open`
- `app_version`
- `platform`
- `ping_schema_version`
- `$ip: null`
- `$process_person_profile: false`

Request envelope:

- `event: "cohort_app_open"`
- `distinct_id: "anonymous-cohort"`

## Controls and transparency

- The `analytics_enabled` toggle controls `dau_app_open`.
- The `Anonymous cohort retention pings` toggle controls `cohort_app_open`.
- Both toggles default to ON if unset.
- `cohort_app_open` is still auto-suppressed for German/Austrian locale/timezone.
- Privacy policy: `Settings -> Privacy & Analytics -> View privacy policy`

## Data location and retention

- `dau_app_open`: existing PostHog US project.
- `cohort_app_open`: PostHog Cloud-EU.
- Retention follows your configured PostHog retention settings and PostHog policy.

## Questions

Use the in-app **Feedback** button for telemetry/privacy questions or concerns.
