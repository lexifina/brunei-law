# How this repository was made (Brunei)

This file is written by the build on 2026-10-30, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Wikidata (CC0) | <https://www.wikidata.org/wiki/Q921> | 2026-10-30 | CC0 1.0 Universal |
| United Nations Treaty Collection (UN Secretary-General as depositary) | <https://treaties.un.org/> | 2026-10-30 | Facts only: treaty names and the dates of signature, ratification, accession or succession |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `legal-system` | Brunei: legal system, from Wikidata (facts only) | 1 | 2026-10-30 to 2026-10-30 |
| `treaties` | Multilateral treaty actions of Brunei (UN Secretary-General as depositary) | 30 | 1984-12-05 to 2020-03-30 |

The build made 31 commits:

| Commits | Kind |
| ---: | --- |
| 2 | first version of an act |
| 29 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-30.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 30 laws in the record.
- 61 tags.

## Dates

Each commit is dated at noon (Asia/Brunei) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Not applicable: this record holds facts and treaty actions, not law text. Each treaty action is dated by the day the depositary records for it; the Wikidata facts carry the day they were read. https://treaties.un.org/

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `57aa9ffafb744567cbf18dd84705935ad89553f3c98e6c2249450d3b8de4b3b8` (43390 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3e59cb6f05eccb94a9ec14431a7f6781221e83ef`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Brunei's official publisher (agc.gov.bn) requires written permission to reproduce, so nothing is taken from it. On 2026-11-26, 93 dated versions of 92 laws were appended on top of this build from secondary copies: FAOLEX (70; https://faolex.fao.org/docs/pdf/) and WIPO Lex (23; https://wipolex-res.wipo.int/edocs/lexdocs/laws/en/bn/). Each commit carries `Source-status: secondary copy (...)`, the PDF's `Source-sha256` and `Text-source` (69 are the publisher's OCR of scanned Gazette prints; no OCR by Lexifina). These commits are not in corpus.json, so `tools/check_repo.py` does not cover them.
- Dating of those versions: the instrument's commencement clause; a Revised Edition's printed day; a Revised Edition listing no amending law (post-1984 laws revised within 10 years) stands for the law as it commenced; FAOLEX or WIPO Lex entry-into-force dates; with no commencement provision, the Gazette date (`Date-basis: published`). Held instead: about 70 texts with no reliable day (mostly Revised Editions without a printed day, and instruments commencing by notification), 3 scans without a text layer, and the Constitution (the Constitute compilations and the WIPO Lex reprint give no dated version). Policies, plans and international agreements in FAOLEX were left out as not national law.
- Not used: Refworld (403 to us), UNODC SHERLOC (no listing we could read without its search application), the ASEAN databases (regional instruments, not Brunei law), archive.org (no Brunei law texts found).
- Wikidata has no dated history for the facts in legal-system, so that act is one version, the oldest available, dated on the day it was read.
- In the treaties act each version adds the treaty actions of one day, dated by the action date, and is credited to a record named for that day.
- Only multilateral treaties deposited with the UN Secretary-General in a fixed list of about 60 were read, so the treaties act is not a complete list of this state's treaty actions.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- none
