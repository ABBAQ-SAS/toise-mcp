# TOISE — MCP server for French land and real estate intelligence

**Endpoint:** `https://mcp.toiseai.com/mcp` (Streamable HTTP) · **Website:** https://toiseai.com · **Official MCP Registry:** `com.toiseai/toise`

TOISE answers the questions of a property or development operation in France, from French public data, with the source and vintage of every figure:

- **Who owns it** — corporate owners (SIREN), their group, directors, BODACC legal notices, financial score, INSEE history.
- **What can be built** — zoning (PLU) and its written rules quoted page by page (including scanned regulations, read by OCR), constraints, risks, buildable capacity in 3D.
- **What it is worth** — DVF transactions, price ranges, developer and operating appraisals, bank-ready files.
- **Where to locate** — catchment areas, transit isochrones, cannibalisation between stores.
- **Sourcing** — vacant plots (dents creuses), pre-emption perimeters, lapsed building permits, owner sale signals, geo-alerts.

71 tools, all read-only except export and private points. TOISE never invents a value: a missing figure is returned as « unavailable », never as zero.

## Connect

| Assistant | How |
|---|---|
| Claude | Custom connector, `https://mcp.toiseai.com/mcp`, with a `toise_sk_…` API key in the `Authorization: Bearer` header |
| ChatGPT | TOISE app in the ChatGPT apps directory |
| Le Chat (Mistral) | Connectors → Add Connector → Custom MCP Connector → URL above, then sign in with your TOISE account |
| Gemini Enterprise | Static OAuth client created by your organisation admin — see https://toiseai.com/gemini-entreprise |
| Any MCP client | Remote MCP server, URL above, OAuth 2.1 (dynamic client registration) or API key |

Without an account: 10 calls per day per IP on light tools. Free account: no credit card. Pricing: https://toiseai.com/offres

## Example prompts (French)

- « Qui possède le 28 rue Rochebrune à Montreuil, et que dit le PLU ? »
- « Quelle capacité constructible sur cette parcelle, et quelle charge foncière en logement ? »
- « Liste les dents creuses de plus de 300 m² à Rennes. »

## About

Published by ABBAQ SAS (France). Support: contact@toiseai.com. This repository only describes the hosted service; the server source code is not public.
