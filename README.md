# dibby-translations

Central source of truth for Dibby user-facing copy.

## Structure

- `common/`: shared brand, navigation, status, and action labels.
- `portal/`: DibbyPortal-specific dashboard, receipts, and profile UI.
- `iam/`: DibbyIAM Razor Pages copy.
- `iam-emails/`: DibbyIAM transactional email copy.
- `marketing/`: dibby.nl marketing site copy.
- `ecommerce/`: e-commerce demo client copy.
- `mobile/`: shared source strings for future native app builds.

Each folder contains one JSON file per locale, using ISO 639-1 locale codes such as `en.json` and `nl.json`.

## Contribution Flow

1. Open a pull request against `main`.
2. Keep every locale file in a folder structurally aligned.
3. A reviewer checks key parity and user-facing wording before merge.

## Key Conventions

- Use dot-style semantic names at the call site, represented as nested JSON objects.
- Use camelCase for key parts.
- Use i18next interpolation syntax: `{{count}}`, `{{name}}`.
- Use i18next plural suffixes: `_one` and `_other`.
- English is the fallback locale. Missing target-locale keys should fall back to `en`.
