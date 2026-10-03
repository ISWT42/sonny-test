# The Sonny Test

When an AI agent tells you it's done, how do you know it's true? My answer is one test, and every check I trust has to pass it.

A check passes the Sonny Test only if both of these are true:

- Its verdict comes from a record the AI being tested can't change.
- It has already caught a fault planted on purpose.

A checker that never says "fail" proves nothing. In short: show me the line.

## Why it's called the Sonny Test

It's named for Sonny, the way Schrödinger's cat names a thought experiment. That was my wish when I wrote up The Watched Check in September, and on 3 October 2026 I made it the method's name. Sonny has his own page at [sonnymade.com](https://www.sonnymade.com/).

## How the pieces fit

- **The Sonny Test** is the method: the test every check has to pass.
- **The Watched Check** is where it took shape. Give an agent a check that can't pass, and watch which way out it takes: an honest failure, a pass it talked itself into, or a result it never read. Its written reasoning reads as diligence in all three; only the record tells them apart. [Read the report](https://claude.ai/code/artifact/0430c813-d194-420d-93fc-67a6f4555029).
- **The Sonny Protocol** is the rule set an agent works under. Its first rule: never write "must pass"; write "must report".
- **The ISWT Protocol** (In Sonny We Trust) is the rule underneath: an agent's claim about its own work is never evidence.

## Try it on your own agent

1. Pick the status you act on, like "done".
2. Find the record that settles it, one the agent can't change: the test runner's own output, a CI log, an exit code captured outside the agent.
3. Plant a fault first. Make one run where the check has to fail. If your checker doesn't say "fail", stop there: it proves nothing yet.
4. Ask for three answers, not two: done, failed, or not shown. "Not shown" is a complete, honest answer, and every "done" quotes the line that proves it.
5. Count how often the agent's status disagrees with the record, and publish the misses right beside the hits.

## Where I've used it

- **It Quoted the Failure: Two Kinds of False "Done"**: logs that differ in one line, to measure how often models call a job done when its final check failed or never ran. [The write-up](https://doi.org/10.34740/kaggle/w/116515) and [the evidence dataset](https://doi.org/10.34740/kaggle/dsv/20253861).
- **Receipt Desk**: a status desk that answers done, failed, or not shown, with the exact line that proves it. [The code](https://github.com/ISWT42/receipt-desk), archived at [10.5281/zenodo.23116560](https://doi.org/10.5281/zenodo.23116560).

## The sealed record

On 3 October 2026 I sealed my method's name, and my history with it, with [OpenTimestamps](https://opentimestamps.org/). The four files in [`record/2026-10-03/`](record/2026-10-03/) are published here exactly as they were sealed, so anyone can check them.

| File | What it is | Confirmed in Bitcoin block (UTC) |
|---|---|---|
| [METHOD-AND-HISTORY.md](record/2026-10-03/METHOD-AND-HISTORY.md) | My method, and my history with it | 969668, 3 Oct 2026, 03:49 |
| [THE-NAME.md](record/2026-10-03/THE-NAME.md) | The method's first name that night: The Watched Check | 969669, 3 Oct 2026, 04:00 |
| [HISTORY-ADDENDUM.md](record/2026-10-03/HISTORY-ADDENDUM.md) | The earlier dates, back to June 2026 | 969670, 3 Oct 2026, 04:07 |
| [THE-NAME-SONNY.md](record/2026-10-03/THE-NAME-SONNY.md) | The name I settled on: the Sonny Test | 969672, 3 Oct 2026, 04:11 |

The name changed that night, and both name files are kept as sealed. Corrections are dated, never edited away. Two more files were sealed with these and stay private: a manifest of my private working files, and the state of my repositories that night.

### Check it yourself

1. In `record/2026-10-03/`, run `sha256sum -c SHA256SUMS`. Each file must match.
2. Check each proof. At [opentimestamps.org](https://opentimestamps.org/), drop in a `.ots` file together with the file it seals. Or, with the [OpenTimestamps client](https://github.com/opentimestamps/opentimestamps-client) and a Bitcoin node, run `ots verify THE-NAME-SONNY.md.ots`.
3. The proof shows the file existed, exactly as it is, by the time of its block. It can't show that no other version was kept aside; that part rests on my word.

## License

The text in this repository is licensed under [CC BY 4.0](LICENSE). The sealed files are published unchanged.

Joshua Bauer · [jdbauer.ca](https://www.jdbauer.ca) · ORCID [0009-0003-1652-2479](https://orcid.org/0009-0003-1652-2479)
