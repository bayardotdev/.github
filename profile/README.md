<p align="center">
  <a href="https://bayar.dev"><img alt="bayar.dev" src="https://img.shields.io/badge/bayar.dev-site-7ee7ff?style=flat-square&labelColor=0d1117"></a>
  <a href="https://bayar.dev/docs"><img alt="Docs" src="https://img.shields.io/badge/docs-read-a78bfa?style=flat-square&labelColor=0d1117"></a>
  <a href="https://bayar.dev/log"><img alt="Dev log" src="https://img.shields.io/badge/dev_log-read-3fb950?style=flat-square&labelColor=0d1117"></a>
  <a href="https://x.com/bayardotdev"><img alt="X" src="https://img.shields.io/badge/X-@bayardotdev-e6edf3?style=flat-square&logo=x&logoColor=white&labelColor=0d1117"></a>
</p>

# bayar.dev

AI infrastructure you can curl, built in public by [@namchinbayar](https://github.com/namchinbayar).

bayar.dev is the layer between users and the model. Today that is one live streaming endpoint with rate limiting and request validation in front of Claude Haiku 5.5, and every number on the site is measured, not claimed.

```sh
curl -N -X POST https://bayar.dev/api/chat -d @prompt.json
```

### What a request looks like

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/namchinbayar/namchinbayar/main/assets/flow-dark.svg">
  <img alt="Live request flow: client → per-IP rate limit → validation → Claude Haiku 5.5 through the Anthropic API → stream back. Planned, not shipped: provider failover, PII guard, semantic cache, private VPC and BYOK" src="https://raw.githubusercontent.com/namchinbayar/namchinbayar/main/assets/flow-light.svg" width="100%">
</picture>

| | |
| --- | --- |
| **Live** | Streaming chat over SSE · 10 requests a minute and 100 a day per IP · schema, role and size validation · hourly benchmarks with public raw data |
| **Next** | Provider failover · PII guard · semantic cache · private VPC / BYOK. Planned, not shipped |
| **Later** | Founders access: tools for people who support the work |

### Measured, not claimed

<!-- BENCH:START -->
<p>
  <a href="https://bayar.dev/benchmarks">
  <img alt="TTFT p50: 510 ms" src="https://img.shields.io/badge/TTFT%20p50-510%20ms-7ee7ff?style=flat-square&labelColor=0d1117">
  <img alt="output p50: 191 tok/s" src="https://img.shields.io/badge/output%20p50-191%20tok%2Fs-a78bfa?style=flat-square&labelColor=0d1117">
  <img alt="success: 100%" src="https://img.shields.io/badge/success-100%25-3fb950?style=flat-square&labelColor=0d1117">
  <img alt="samples: 141" src="https://img.shields.io/badge/samples-141-8b949e?style=flat-square&labelColor=0d1117">
  </a>
</p>

<sub>Claude Haiku 5.5 (low effort), short chat, last 7 days, probed every hour. Method and raw data at <a href="https://bayar.dev/benchmarks">bayar.dev/benchmarks</a>.</sub>
<!-- BENCH:END -->

### Latest from the log

<!-- LOG:START -->
- [The homepage is one prompt now, with a tide under it](https://bayar.dev/log/the-homepage-is-one-prompt-with-a-tide-under-it) · <sub>Nov 14, 2026</sub>
- [What enforcing the CSP cost, and what it could not see](https://bayar.dev/log/what-enforcing-the-csp-cost-and-what-it-could-not-see) · <sub>Nov 14, 2026</sub>
- [The homepage now leads with numbers I measure](https://bayar.dev/log/the-homepage-now-leads-with-numbers-i-measure) · <sub>Nov 14, 2026</sub>
- [All entries →](https://bayar.dev/log)
<!-- LOG:END -->

### Links

- [Docs](https://bayar.dev/docs): request schema, streaming protocol, limits and errors
- [Benchmarks](https://bayar.dev/benchmarks): method, every model, raw data
- [Projects](https://bayar.dev/projects): what else I build and use every day
- [Privacy](https://bayar.dev/privacy) · [About](https://bayar.dev/about)
- [hi@bayar.dev](mailto:hi@bayar.dev) · [LinkedIn](https://www.linkedin.com/in/bayardev)
