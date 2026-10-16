# Contributing

Keep Ascent's reusable workspace concepts independent of personal instruction hierarchies, machine paths, installation managers, and domain-specific research or development policies.
The canonical workflow is `skills/ascent/SKILL.md`; optional hook mechanics belong in its linked hook guide.
Keep the skill self-contained when installed independently of this repository.

The hook only observes bounded, selected project documents and returns host-compatible continuation requests.
It must not write workspace documents, follow target links, call a model service, modify trust settings, or infer task completion from an event.
Changes to counters and pending file sets must remain safe under concurrent sessions and repeated events.
Retain the distinction between requesting refinement and verifying that it was performed.

Run the behavioral checks from the repository root:

```bash
python3 -m unittest discover -s tests -v
```

Also run the available skill validator when changing the skill.
Test both supported event payloads and failure behavior; non-Ascent, malformed input, unsupported events, and read-only plan mode must not produce continuation requests.
Run native Windows checks when available before claiming Windows execution was verified.
Keep generated indexes, caches, runtime state, and installation-specific records out of tracked source.
