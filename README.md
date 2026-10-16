# Nothing But Alpha: ledger heads

This repository holds the **daily fingerprints ("heads") of Nothing But Alpha's forecast ledger**, and nothing else.

Every forecast we record goes into an append-only, hash-chained ledger. At the end of each day we seal it and commit one line here: the date, the number of records, a Merkle root of that day's records, and the hash of the chain so far.

Committing that line publicly, with GitHub's timestamp and history, means:

- **We can't quietly change the past.** Editing, deleting, reordering or backdating any forecast changes the hashes and no longer matches the head published here on that date.
- **Anyone can check us.** When the full ledger is published, a short standalone script can recompute every head and compare it against this repository.

The forecasts themselves are not in this repository. A head reveals nothing about what was forecast.

Nothing here is investment advice, and no performance is claimed. This is a record-keeping mechanism.

Format: `heads/heads.jsonl`, one JSON object per sealed day. The specification will be published with the ledger.
