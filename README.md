# Klisten PatchProof — status companion (limited review beta)

Read an existing verification using its UUID and your own organization's Klisten API key with `verify:read`. This Claude Code plugin exposes exactly one tool: `patchproof_status`.

## What it returns

State, result, creation/completion timestamps, and whether a report and signed receipt are present. Receipt presence is **not** signature verification. Report bodies, arbitrary reasons, repository source and credentials are not returned.

## What it does not do

No upload, submission, code execution, cancellation, payment, or fund transfer. It does not verify arbitrary repositories, languages, vulnerabilities, or AI identity. The available execution trial is an explicitly enrolled fixed C11 arithmetic fixture. New users cannot assume a general-purpose verification service is available. Contact klisteninc@gmail.com for availability before relying on this limited beta.

## Connect

Configure `user_config.api_key` with your own `verify:read` key. HTTPS endpoint: https://api.klisten.co.kr/mcp/patchproof (Streamable HTTP). Never commit keys. Provide the UUID of an existing job in the same organization. Ask: “Check the status of my PatchProof verification ID.” Do not poll more frequently than once every 10 seconds.

## Limits and review window

The current separately authorized fixed-fixture review window ends 2026-10-17 at 12:01:20 UTC. Access may be disabled when the window ends; ongoing public availability is not promised. The plugin never runs the fixture. The MCP has bounded input/output, a 5-second upstream timeout with no retries, global 60 requests/minute and persistent daily limits. Busy or unavailable responses are errors, never successful verification.

## Verification

On 2026-10-10 the public HTTPS endpoint passed initialize, tools/list, own-organization tools/call, foreign-organization denial, and blocked execution-tool tests. The separate fixed-fixture request completed VERIFIED_PASS; its Ed25519 signature and evidence hash were checked outside the MCP. These observations do not certify arbitrary code safety.

## Data and policies

Calls send a verification UUID and API key to Klisten over HTTPS. Access logs may be retained; no zero-retention claim is made. Do not submit secrets in prompts. Privacy: https://klisten.co.kr/privacy.html · Terms: https://klisten.co.kr/terms.html · Documentation: https://klisten.co.kr/docs.html · Support: klisteninc@gmail.com.

No private review credential, customer data, hooks, local executable, or undeclared command is included in this package.
