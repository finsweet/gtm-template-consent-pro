# Consent Pro — Google Tag Manager Template

Google Tag Manager tag template for [Consent Pro](https://consentpro.com) v2. Integrates Consent Pro with [Google Consent Mode](https://developers.google.com/tag-platform/security/guides/consent) by setting region-specific defaults, reading user choices from the `fs-consent` cookie, and updating consent state in GTM.

## Install from the Community Template Gallery

Once published, add this template from the [GTM Community Template Gallery](https://tagmanager.google.com/gallery):

1. Open your GTM container → **Templates** → **Search Gallery**
2. Search for **Consent Pro**
3. Click **Add to workspace**

## Manual install

1. Download [`template.tpl`](./template.tpl) from this repository
2. In GTM, go to **Templates** → **New** → menu (⋮) → **Import**
3. Select `template.tpl` and save

## Setup

Full setup instructions: [How to Set Up Google Tag Manager with Consent Pro V2](https://docs.consentpro.com/v2/google-tag-manager-setup)

Summary:

1. Create a tag using this template
2. Configure region-specific consent defaults to match your Consent Pro instance
3. Set the trigger to **Consent Initialization - All Pages**
4. Publish your container

### Consent Mode mappings

| Consent Pro category | GTM consent types |
| -------------------- | ----------------- |
| `essential` | `security_storage` (always granted) |
| `analytics` | `analytics_storage` |
| `marketing` | `ad_storage`, `ad_user_data`, `ad_personalization` |
| `personalization` | `functionality_storage`, `personalization_storage` |

## Publishing updates to the gallery

1. Edit the template in GTM and export `template.tpl`
2. Replace `template.tpl` in this repo and commit
3. Copy the commit SHA: `git rev-parse HEAD`
4. Add a new entry at the top of `versions` in `metadata.yaml` with the SHA and change notes
5. Commit `metadata.yaml` and push — the gallery updates within 2–3 days

## Submitting to the gallery (first time)

1. Commit all files to `main` on this repository
2. Update `metadata.yaml`: replace `REPLACE_WITH_COMMIT_SHA` with the commit SHA that includes `template.tpl`
3. Commit the metadata change and push
4. Ensure **Issues** are enabled on the GitHub repository
5. Go to [tagmanager.google.com/gallery](https://tagmanager.google.com/gallery) → **Submit Template** → paste this repo URL

## Support

- Documentation: [docs.consentpro.com](https://docs.consentpro.com/v2/google-tag-manager-setup)
- Issues: [github.com/finsweet/gtm-template-consent-pro/issues](https://github.com/finsweet/gtm-template-consent-pro/issues)

## License

Apache License 2.0 — see [LICENSE](./LICENSE).
