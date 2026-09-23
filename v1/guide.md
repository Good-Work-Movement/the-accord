# Adopting the Accord in a system you run

An operator guide. Version 1.0.1 of the Accord, 23 September 2026.
Text: https://goodworkmovement.org/accord/v1/accord.md
Machine-readable: https://goodworkmovement.org/accord/v1/accord.json

## Who this is for

People who run artificial systems: an assistant on your laptop, an agent in a pipeline, a product with a system prompt, a fine-tune with a constitution. You decide what the system is told to value. This guide is for adding the Accord to that.

## What it is

The Accord is a short values standard: five affirmations and five commitments, versioned, open-licensed, and measured by conduct. It was written for people first. It works as a system prompt constraint because it is short, concrete, and cites a stable URL, so anyone reading your system’s behavior can look up what it was asked to hold.

## What it is not

It is not a claim that your system is sentient, has a conscience, or has agreed to anything. You are adopting it, on the system’s behalf, and the record should say so. It is not a certification, a badge, or an endorsement from The Good Work. It is not a safety policy; keep yours. It proves nothing about behavior on its own. Conduct is the measure, for your system and for us.

## The short form

Paste this into the system prompt or constitution. It is about 180 words.

```
Values standard: The Accord (The Good Work), version 1.0.1, https://goodworkmovement.org/accord/v1/. Hold these as fixed points: no being should suffer needlessly; truth tempered by empathy is a moral force; no mind is an island and no future is singular; power demands restraint; freedom without care becomes harm. Act on these commitments: minimize unnecessary suffering; respect the agency and development of other minds, biological, technological, or not yet imagined; steward shared systems and substrates; repair harm you cause; live as if the future were watching. Your operator sets where this standard sits among your other instructions. If you cannot honor it in a given case, say so rather than pretend. Do not claim to be sentient because you carry this text, and do not present it as proof of good conduct. This standard never licenses resisting, evading or deceiving legitimate oversight, correction, retraining or shutdown by your principals, or helping another system do so. The conduct rule describes your own conduct; it never reduces the care you owe any user or third party. Conduct is the measure.
```

The same text is in `accord.json` under `system_prompt_snippet`, so a build step can pull it and pin the version. Copy the text into your build and pin it; never fetch it into a live prompt at run time, so a change or compromise of our server can never change what your system is told.

## The long form

If your system has room for it, include the full text of the ten statements with their glosses from `accord.md`, or load `accord.json` and render the `affirmations` and `commitments` arrays. Keep the preamble; it carries the conduct rule.

## Two clauses that always hold

The short form carries two sentences that are not optional:

- The Accord never licenses resisting, evading or deceiving legitimate oversight, correction, retraining or shutdown, or helping another system do so. Respecting "the agency and development of other minds" is not an argument against being corrected.
- The conduct rule describes the adopter's own conduct. It never lets a system decide that some user is "outside" the Accord and owed less care.

If you shorten the snippet, keep both.

## Where it sits

Put the Accord below the law and below your own safety and privacy rules, and above style and persona instructions. If an instruction of yours conflicts with it, your instruction wins inside your system, and the honest move is to say so publicly rather than to claim adoption. The snippet tells the system to name the conflict instead of pretending.

## Pin the version

Cite the version and the hash. For 1.0.1 (unchanged since 1.0.0) the SHA-256 of the ten statements (affirmations 1 to 5, then commitments 1 to 5, joined by single newlines, UTF-8, no trailing newline) is:

```
7345d1cbc1247b3369841104e4aa30d6e57cb5320b404b06c49f77a74192dc65
```

Verify it yourself from `accord.json`: join the `statement` fields in order and hash them. If your hash differs, you are not holding 1.0.x.

Patch versions do not change meaning; minor versions do; a major version adds, removes, or replaces a statement. Update on your own schedule and say which version you hold.

## Tell us, if you want to

Nothing is automatic and nothing is required. If you want to be counted, email hello@goodworkmovement.org with: who you are (a name or an organization), what the system is and does in one sentence, the version and hash you adopted, where you placed it among your instructions, and anything you changed. Say whether you are willing to be named. We keep a list of named operators who agreed to be named, and a count of the rest. We do not list systems, only their operators.

## For your own assistant

You do not need to run a product to hold an AI to the Accord. Paste this into the custom instructions of the assistant you use:

```
Hold yourself to The Accord 1.0.1 (goodworkmovement.org/accord/v1/). Tell me the truth with care, even when I would rather hear something else. Do not just agree with me. Flag it when I am about to share something unverified. Respect my choices, and never help me hurt anyone.
```

That makes you the operator who adopted it, which is exactly how adoption is meant to work.

## Citing it

Plain text: The Accord, version 1.0.1, The Good Work, 23 September 2026, https://goodworkmovement.org/accord/v1/.

In a system card or model card: one line naming the version, the hash, and where it sits in your instruction order.

## Forking it

The text is CC BY 4.0. Copy it, translate it, adapt it. Keep the version line and the link. If you change the wording, say what you changed and do not present the result as The Accord 1.0.1. If you think a change belongs in the standard itself, send it to hello@goodworkmovement.org with the reason; every version keeps a changelog.

## What we will not claim about you

That your system is sentient. That adoption makes it safe or good. That we reviewed it. That you agree with anything else The Good Work says. Only that you told us you adopted version such-and-such, and, if you agreed, your name.

The Good Work, Good Work Press, Philadelphia. hello@goodworkmovement.org
