# Brunei: law history in git (metadata only, no law text)

**This repository holds no law text.** The text of Brunei's laws is not published here because the Attorney General's Chambers site terms do not allow the laws to be republished and no permission or licence has been given. What is here is facts only, so the repository has something real in it and the history can grow when the laws can be added.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law): one file per unit, one commit per record on its day, and the record that made each change as the commit's author.

**What is in it now**

| Folder | Content | Versions | History |
| --- | --- | ---: | --- |
| `legal-system/` | Facts from Wikidata: government, institutions, legal instruments recorded there | 1 | Read on 2026-10-30 (no dated history exists) |
| `treaties/` | Treaty actions at the UN Treaty Collection | 30 | One version per day with an action (26 treaties) |

**Language.** English. Names are as given by Wikidata and the UN Treaty Collection.

## Sources

- Wikidata, under CC0 (https://www.wikidata.org/wiki/Q921): facts about Brunei and records that its legal instruments exist.
- UN Treaty Collection (https://treaties.un.org/): treaty names and the dates of signature, ratification, accession or succession, for about 60 of the main multilateral treaties deposited with the UN Secretary-General. This is not a full list of the state's treaty actions.

## Dates

The treaties history is dated by the day the depositary records for each action. The Wikidata facts have no dated history, so they are one version dated on the day they were read (2026-10-30).

## How it is checked

Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`) and must match `corpus.json`; results are in `REPRODUCE.md`.

## What "author" means

The author of a commit is the record that made the change, with an e-mail address that cannot exist. The committer is always Lexifina.

## Limits

No law text. Wikidata can be incomplete or wrong. The treaties list covers only a fixed set of about 60 multilateral treaties.
