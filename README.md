# dsh monitor

Encrypted, monitoring-only static page of what dsh produced (task state, turns, tool-call counts, outputs, errors, autoloop runs).

- The published `index.html` is **ciphertext only** (AES-256-GCM, PBKDF2-SHA-256). The password is not in this repository.
- A **wrong password shows nothing** (the page does not decrypt and does not render any data).
- Refreshed about every 15 minutes by a **local** script (`bash` + `python` + `git push`) on the operator machine. The loop makes **no LLM calls, no Grok Bot routine calls, and no MCP connector calls**, and uses **zero** dsh / Grok Bot quota.
- Git push uses a locally stored GitHub credential, configured once (`gh auth` / git credential helper).

Open the GitHub Pages URL and enter the operator password.
