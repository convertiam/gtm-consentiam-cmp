# Consentiam CMP — Google Tag Manager Template

Lightweight cookie consent banner with **Google Consent Mode v2** support.
GDPR & ePrivacy compliant. Under 3 KB gzip for recurring visitors.

## Features

- **Google Consent Mode v2** — All 7 consent signals supported
- **EEA region targeting** — Enabled by default for European compliance
- **Two installation modes** — Automatic (API) or Optimized (instant render)
- **Microsoft Consent Mode** — Optional support for Clarity + Bing Ads
- **Multi-language** — 15+ languages with auto-detection or manual override
- **Shadow DOM isolation** — No CSS conflicts with your site
- **Ultra-lightweight** — ~3 KB gzip recurring, ~10 KB first visit

## Installation

1. In Google Tag Manager, go to **Templates → Search Gallery**
2. Search for **"Consentiam CMP"**
3. Click **Add to workspace**
4. Create a new **Tag** with trigger **Consent Initialization — All Pages**
5. Enter your **Consentiam API Key**
6. *(Optional)* Paste your **Config Code** from the dashboard for instant rendering
7. Save and publish

## Configuration

| Parameter | Default | Description |
|-----------|---------|-------------|
| **API Key** | *(required)* | Your Consentiam API key from the dashboard |
| **Config Code** | *(empty)* | Base64 config for instant rendering without API fetch |
| **Wait for Update** | `500` ms | Time to wait before firing tags with default consent |
| **Regions** | `eea` | Consent applies to these regions. Use `all` for global, `eea` for Europe, or comma-separated ISO 3166-2 codes |
| **Microsoft Consent** | `off` | Enable consent signals for Microsoft Clarity and Bing Ads |
| **Language** | `auto` | Banner language. Auto-detect reads HTML lang, URL path, and browser settings |

## How It Works

1. The template sets **all consent signals to `denied`** by default (GDPR-safe)
2. If a consent cookie exists, it **updates consent** to the user's saved preferences
3. It injects the lightweight Consentiam banner script from CDN
4. The banner handles user interaction (Accept All / Reject All / Customize)
5. Consent choices are stored and synced with Google Consent Mode v2

## Consent Signal Mapping

| Category | Google Consent Mode Signals |
|----------|-----------------------------|
| Analytics | `analytics_storage` |
| Marketing | `ad_storage`, `ad_user_data`, `ad_personalization` |
| Preferences | `functionality_storage`, `personalization_storage` |
| Necessary | `security_storage` *(always granted)* |

## Documentation

- [GTM Installation Guide](https://www.consentiam.eu/docs/gtm)
- [Google Consent Mode](https://www.consentiam.eu/docs/gcm)
- [GDPR Compliance](https://www.consentiam.eu/docs/gdpr)
- [Consentiam Dashboard](https://www.consentiam.eu/dashboard)

## Support

- [Open an issue](https://github.com/convertiam/gtm-consentiam-cmp/issues) on GitHub
- Email: soporte@consentiam.eu
- Website: [www.consentiam.eu](https://www.consentiam.eu)

## License

[Apache 2.0](LICENSE)

Developed by [Convertiam.com](https://www.convertiam.com)
