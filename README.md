# Open Regulatory AI Framework

Open, community-reviewable taxonomy + prompt + retrieval framework for pharmaceutical regulatory intelligence.

**Current jurisdictions**
- 🇨🇳 China — NMPA / CDE / CFDI
- 🇺🇸 United States — FDA / CDER / CBER / eCFR
- 🇪🇺 European Union — EMA / European Commission / EudraLex / EUR-Lex

## What this repository provides

- shared product taxonomy;
- lifecycle taxonomy;
- GxP topic taxonomy;
- jurisdiction-specific regulatory source registries;
- keyword / synonym maps;
- regulatory query-builder prompts;
- applicability and change-impact prompts;
- safety rules for prompt injection, fabricated citations, outdated law, and evidence handling;
- issue / pull-request templates for community review.

## Architecture

```text
User question
  ↓
Intent + jurisdiction
  ↓
Product type / lifecycle / GxP topic
  ↓
Jurisdiction taxonomy
  ↓
Official-source query plan
  ↓
Evidence retrieval
  ↓
Applicability + current-status check
  ↓
Cited answer
  ↓
Qualified human review
```

## Jurisdiction packages

The umbrella repository contains all three jurisdiction packages and each region is also available as an independent public repository:

- 🇨🇳 [China / NMPA](https://github.com/nayihoney-spec/open-regulatory-ai-nmpa) — local folder: `jurisdictions/cn-nmpa/`
- 🇺🇸 [United States / FDA](https://github.com/nayihoney-spec/open-regulatory-ai-fda) — local folder: `jurisdictions/us-fda/`
- 🇪🇺 [European Union / EMA](https://github.com/nayihoney-spec/open-regulatory-ai-eu-ema) — local folder: `jurisdictions/eu-ema/`

## Open-core boundary

This public framework describes regulatory knowledge structure and safe retrieval patterns. It intentionally does **not** publish proprietary enterprise orchestration, customer knowledge bases, private credentials, commercial validation packages, customer-specific workflows, or proprietary Aves AI Hub runtime implementation.

## Safety

Read [DISCLAIMER.md](DISCLAIMER.md), [SECURITY.md](SECURITY.md), and [SELF_CHECK.md](SELF_CHECK.md) before using the framework.

Run the local static check:

```bash
python tools/repo_self_check.py .
```

The checker uses only the Python standard library and does not access the network.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Regulatory corrections should include an official source URL.

## Support

This project is free to use. See [SUPPORT.md](SUPPORT.md). A GitHub Sponsors configuration for `@nayihoney-spec` is included in `.github/FUNDING.yml`; the Sponsor button becomes functional after GitHub Sponsors onboarding/approval is active for the maintainer.

## License

Knowledge content: CC BY 4.0.  
Tools under `tools/`: Apache-2.0.  
See [LICENSE.md](LICENSE.md).
