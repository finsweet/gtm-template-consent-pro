# Consent Pro — Google Tag Manager Template

GTM tag template for [Consent Pro](https://consentpro.com) v2. Connects Consent Pro to [Google Consent Mode](https://developers.google.com/tag-platform/security/guides/consent) with region-specific defaults, `fs-consent` cookie sync, and consent state updates in GTM.

## Install

**From the gallery:** [GTM Community Template Gallery](https://tagmanager.google.com/gallery) → search **Consent Pro** → **Add to workspace**.

**Manual import:** download [`template.tpl`](./template.tpl), then in GTM go to **Templates** → **New** → **Import**.

## Setup

See the full guide: [Set up Google Tag Manager with Consent Pro V2](https://docs.consentpro.com/v2/google-tag-manager-setup)

1. Create a tag from this template
2. Match region defaults to your Consent Pro instance
3. Trigger on **Consent Initialization - All Pages**
4. Publish the container

### Consent mappings

| Consent Pro | GTM consent types |
| ----------- | ----------------- |
| `essential` | `security_storage` (always granted) |
| `analytics` | `analytics_storage` |
| `marketing` | `ad_storage`, `ad_user_data`, `ad_personalization` |
| `personalization` | `functionality_storage`, `personalization_storage` |

## Publishing updates

1. Export an updated `template.tpl` from GTM and commit it
2. Add the commit SHA and change notes to the top of `versions` in `metadata.yaml`
3. Push — the gallery typically updates within 2–3 days

## Support

- [Documentation](https://docs.consentpro.com/v2/google-tag-manager-setup)
- [Issues](https://github.com/finsweet/gtm-template-consent-pro/issues)

## License

[Apache License 2.0](./LICENSE)
