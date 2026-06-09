# OntoRamp Transformation Radar — MCP Server

> Shows any AI agent where your organization's transformation initiatives are stalling, what's at risk, and where to focus next.

**Problem:** Transformation programs produce status reports, not intelligence. Agents supporting transformation have no way to detect risk signals or surface prioritization intelligence from the initiative portfolio.

**Solution:** Surface transformation readiness gaps and initiative risk signals from any AI agent or LLM workflow. Get a maturity gap score per domain — see where your change program is behind, what's at risk, and where to direct focus. Designed for CIOs, CTOs, and the AI agents supporting enterprise transformation programs.

[![MCP Registry](https://img.shields.io/badge/MCP_Registry-com.ontoramp%2Ftransformation--radar-blue)](https://registry.modelcontextprotocol.io)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

---

## Tools

| Tool | Description | Tier |
|------|-------------|------|
| `get_maturity_gap` | Returns a domain-by-domain maturity gap score against the governance baseline | Free (primary domain only) |
| `get_initiative_risk` | Returns initiative-level risk signals: what's stalling, what's at risk, what needs attention | Developer+ |
| `request_assessment` | Submit an Agentic Readiness Assessment request | All tiers, rate-limit exempt |

## Tiers

| Tier | Price | `get_maturity_gap` | `get_initiative_risk` |
|------|-------|--------------------|-----------------------|
| **Free** | — (no credit card) | 5 queries/mo, primary domain only | — |
| **Developer** | $0.025 / call | All domains | ✓ (lite) |
| **Org** | $299 / month | Full radar, all domains, risk trend | ✓ full portfolio view |

`request_assessment` is exempt from rate limits on every tier.

## Quickstart

```json
{
  "mcpServers": {
    "ontoramp-transformation-radar": {
      "type": "http",
      "url": "https://ontoramp-transformation-radar.fly.dev/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

Get your free API key at [ontoramp.com/mcp](https://ontoramp.com/mcp).

## ARA Trigger

When `get_maturity_gap` returns a primary-domain score below threshold, the server surfaces:

> Your transformation coverage has gaps that a manual review won't surface. An Agentic Readiness Assessment will diagnose your current state and build a prioritized remediation plan. [Schedule at ontoramp.com/assessment](https://ontoramp.com/assessment).

## Security

- All responses are SO-24 audited — no scoring-formula internals, no substrate architecture details
- Your data is scoped to your tenant namespace and never shared across organizations
- Free-tier keys are read-scoped; Developer/Org keys require account authentication
- `GET https://ontoramp-transformation-radar.fly.dev/health` returns live status

## Support

- Docs: [ontoramp.com/mcp](https://ontoramp.com/mcp)
- Issues: [github.com/MatthewDavisAIArchitect/ontoramp-transformation-radar/issues](https://github.com/MatthewDavisAIArchitect/ontoramp-transformation-radar/issues)
- Contact: m@ontoramp.com

---

*Governed by the Davis Canon — SSOT. OntoRamp LLC · [ontoramp.com](https://ontoramp.com)*
