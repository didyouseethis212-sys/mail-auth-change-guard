# Mail Auth Change Guard

**[Try the free browser comparison](https://mail-auth-change-guard.hjbjm.chatgpt.site)** — no signup, mailbox connection or DNS access. Your XML stays on your device.

Compare consecutive DMARC aggregate report batches for IT agency review. Flag new failing IPs, previously aligned sources now failing, failure-rate increases and changed reported policies. Equivalent parsed repeat reports are counted once within a batch; conflicts and overlapping receiver windows are rejected.

## Reproduce the example

Load the synthetic example, then compare. Baseline100 receiver observations/0failures; current110/30failures(27.2727%). Expected3findings. These are synthetic reports and documentation IPs, not customers or real mail.

- [Synthetic input and expected output](https://mail-auth-change-guard.hjbjm.chatgpt.site/example.json)
- [Offline Python package](https://mail-auth-change-guard.hjbjm.chatgpt.site/mail-auth-change-guard.zip)
- [n8n setup starter](https://mail-auth-change-guard.hjbjm.chatgpt.site/n8n.json) — requires your own API key; API access is available through RapidAPI. This starter is not a published n8n-library template or n8nCloud validation claim.

## Important distinctions

Uses `policy_evaluated` alignment, not raw authentication results. Either aligned SPF or DKIM suffices for the pass count. Counts are receiver observations, not unique emails or inbox delivery. Source ownership, legitimacy and spoofing are not inferred. Caller must confirm comparable report coverage; complete coverage is unknown. No DNS changes or enforcement recommendation.

Supports1–20 uncompressed XML reports per period, each256KiB/5000records. Required-field subset of legacy unnamespaced XML and RFC9990 namespace, not full XSD validation. No gzip/ZIP/forensic reports. Same domain and reporter sets, nonoverlapping baseline/current windows. Deduplication is within supplied batches, not persistent storage.

The browser checker is free. [API plans](https://rapidapi.com/didyouseethis212sys/api/mail-auth-change-guard/pricing): BASIC$0/25requests per month; PRO$9/500requests per month. Hard request limits apply; platform bandwidth fees and workflow hosting costs are separate. The synthetic request returned HTTP200 through RapidAPI. [Free Postmark summaries](https://dmarc.postmarkapp.com/) and self-hosted scripts are alternatives; the purchase hypothesis is repeated batch comparison inside an existing agency workflow, not a generic summary replacement.

## Verification

Python unit tests11passed; CLI output verified. JavaScript engine matched the Python synthetic fixture; duplicate/conflict/overlap/coverage/XML security and authenticated Worker request checks passed. Public browser example returned3findings. No real customer files, acquired users or paid transactions are claimed.

Maintainer disclosure: this project was built and documented using an AI agent. Review results before acting. If reporting a format error, provide synthetic XML only; private report domains and source IPs should not be posted publicly.

[Aggregate-reporting standard RFC9990](https://www.rfc-editor.org/rfc/rfc9990.html).
