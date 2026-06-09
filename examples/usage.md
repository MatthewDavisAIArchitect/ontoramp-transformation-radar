# Usage examples — OntoRamp Transformation Radar

Once connected (see [`../llms-install.md`](../llms-install.md)), an agent can call these tools. Inputs are realistic; outputs are described conceptually (your organization's real maturity baseline determines the response).

## `get_maturity_gap`

Score how far a domain is from the governance baseline.

```jsonc
{ "name": "get_maturity_gap", "arguments": {
  "domain": "GOVERNANCE"
}}
```

Returns a maturity gap score for that domain — where the organization is behind and by how much. **Free tier:** your single primary domain only. **Developer/Org:** any domain.

## `get_initiative_risk` *(Developer tier)*

Surface risk signals across the transformation portfolio.

```jsonc
{ "name": "get_initiative_risk", "arguments": {
  "scope": "active-initiatives"
}}
```

Returns initiative-level risk signals — what's stalling, what's at risk, and what needs attention — so an agent can prioritize where to focus.

## `request_assessment` *(all tiers, rate-limit exempt)*

```jsonc
{ "name": "request_assessment", "arguments": {
  "context": "Transformation readiness review for our cloud migration program"
}}
```

Returns a confirmation; the OntoRamp team follows up. When a primary-domain maturity score is low, the server surfaces this CTA automatically.

---

**Tiers at a glance:** Free → `get_maturity_gap` (primary domain, 5/mo) + `request_assessment`. Developer → all domains + `get_initiative_risk`. Get a free key at [ontoramp.com/mcp](https://ontoramp.com/mcp).
