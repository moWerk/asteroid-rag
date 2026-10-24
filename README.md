# asteroid-rag

Curated AsteroidOS engineering knowledge, kept as structured JSON so an LLM can
retrieve it instead of guessing. This is the public subset of a larger private
working corpus, synced at stop points rather than continuously.

The investigation files label what is actually known. `confidence` is one of
`confirmed`, `inferred` or `recalled`, and `confirmed` means a named artifact
exists: a device log, a build, a measurement, a PR. There are 161 such labels
across the files below. Findings that turned out wrong are kept with the
correction attached, because the dead ends are the part that saves the next
person time. `watchface_design_spec.json` and the device database are
prescriptive references rather than investigation records, so they carry no
per-entry labels.

## Files

| file | what it holds | confidence-labelled entries |
|---|---|---|
| `qml_patterns.json` | QML gotchas and Qt5 to Qt6 migration patterns | 91 |
| `platform_and_build.json` | Yocto and Qt/QML platform knowledge, dumping and flashing mechanics | 48 |
| `wiki_reference.json` | what the wiki documents and the decisions behind the pages | 12 |
| `visual_design_guide.json` | design language: typography, colour, layout, ambient/AoD, Qt6 layout tuning | 5 |
| `recipe_style_guide.json` | bitbake recipe conventions | 5 |
| `watchface_design_spec.json` | self-contained watchface authoring and Qt6 spec | reference |
| `20260414_device_db_final.json` | per-device database | reference |

## Scope

Held back on purpose: anything carrying a person's private words, machine and
infrastructure records, hardware identifiers, and raw session transcripts. The
corpus rule is that a RAG holds distilled knowledge, not logs.
`platform_and_build.json` is published with ten lines redacted against the
private original; the other six files are byte-identical to it.

Knowledge in here came from AsteroidOS maintainers and contributors, named at
the point of use where it is theirs. Correct the record by opening an issue.

## Licence

Copyright (C) 2026 Timo Könnecke (moWerk) <mo@mowerk.net>

`SPDX-License-Identifier: GPL-3.0-or-later`

This corpus is free: you can redistribute it and/or modify it under the terms
of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version. See [LICENSE](LICENSE). It is distributed in the hope that it will be
useful, but WITHOUT ANY WARRANTY, without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

The licence covers this compilation and its wording. Individual facts about
AsteroidOS are not anyone's to license, and where a finding is a contributor's
it is named at the point of use.
