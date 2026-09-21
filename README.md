# The Accord

A short values standard from The Good Work: five affirmations and five commitments, measured by conduct, not by agreement. Versioned, open-licensed, and machine-readable, so a person can adopt it, an organization can adopt it in writing, and the operator of an artificial system can add it to a system prompt or constitution and cite exactly what was adopted.

Canonical home: https://goodworkmovement.org/accord/v1/ (this repository mirrors those bytes).

## Files

- `v1/accord.md`: the text.
- `v1/accord.json`: the same text as data, with adoption rules, a system prompt snippet, and an integrity hash.
- `v1/accord.schema.json`: JSON Schema for `accord.json`.
- `v1/guide.md`: adopting the Accord in a system you run (operators).
- `v1/CHANGELOG.md`: what changed and when.

## Verify

The integrity hash is SHA-256 over the ten statements (affirmations 1 to 5, then commitments 1 to 5) joined by single newlines, UTF-8, no trailing newline.

```
python3 -c "import json,hashlib;d=json.load(open('v1/accord.json'));s=[a['statement'] for a in d['affirmations']]+[c['statement'] for c in d['commitments']];print(hashlib.sha256('\n'.join(s).encode()).hexdigest()==d['integrity']['hash'])"
```

Version 1.0.0 hash: `7345d1cbc1247b3369841104e4aa30d6e57cb5320b404b06c49f77a74192dc65`

## What adoption is not

Adoption is not certification, and The Good Work issues no badge. An artificial system does not adopt the Accord on its own; its operator does, on its behalf, and the record says so. Nothing here claims that any current system is sentient. Conduct is the measure.

## Contributing

Open an issue for a counterexample, a translation, or a wording problem. Changes to the ten statements are major versions and are decided by the publisher; everything else follows the changelog. Forks are welcome under the license: keep the version line and the link, say what you changed, and do not present a modified text as The Accord 1.0.0.

## License

CC BY 4.0. See `LICENSE`.
