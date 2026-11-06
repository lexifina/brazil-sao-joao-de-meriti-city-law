# How this repository was made (São João de Meriti)

This file is written by the build on 2026-11-06, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Câmara Municipal de São João de Meriti, SAPL: records of the municipal laws and their PDFs (newest first) | <https://sapl.saojoaodemeriti.rj.leg.br/norma/pesquisar> | 2026-11-01 | Texts: Câmara Municipal de São João de Meriti, SAPL (Sistema de Apoio ao Processo Legislativo), sapl.saojoaodemeriti.rj.leg.br; SAPL: "Conteúdo e dados sob licença Creative Commons 4.0 Atribuir Fonte - Compartilhar Igual". Lei 9.610/1998 art. 8 IV: the texts of laws and other official acts are not protected by copyright. Non-official text: only the official gazette is authoritative. |
| Câmara Municipal de São João de Meriti, SAPL: records of the municipal laws and their PDFs (newest first) | <https://sapl.saojoaodemeriti.rj.leg.br/norma/pesquisar> | 2026-11-06 | Texts: Câmara Municipal de São João de Meriti, SAPL (Sistema de Apoio ao Processo Legislativo), sapl.saojoaodemeriti.rj.leg.br; SAPL: "Conteúdo e dados sob licença Creative Commons 4.0 Atribuir Fonte - Compartilhar Igual". Lei 9.610/1998 art. 8 IV: the texts of laws and other official acts are not protected by copyright. Non-official text: only the official gazette is authoritative. |
| Câmara Municipal de São João de Meriti, SAPL: records of the municipal laws and their PDFs (newest first) | <https://sapl.saojoaodemeriti.rj.leg.br/norma/pesquisar> | 2026-11-06 | Texts: Câmara Municipal de São João de Meriti, SAPL (Sistema de Apoio ao Processo Legislativo), sapl.saojoaodemeriti.rj.leg.br; SAPL: "Conteúdo e dados sob licença Creative Commons 4.0 Atribuir Fonte - Compartilhar Igual". Lei 9.610/1998 art. 8 IV: the texts of laws and other official acts are not protected by copyright. Non-official text: only the official gazette is authoritative. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `lei-2026-02816` | Lei nº 2.816, de 31 de agosto de 2026 | 1 | 2026-08-31 to 2026-08-31 |
| `lei-2023-02427` | Lei nº 2.427, de 10 de outubro de 2023 | 1 | 2023-10-10 to 2023-10-10 |
| `lei-2022-02335` | Lei nº 2.335, de 14 de junho de 2022 | 1 | 2022-06-14 to 2022-06-14 |
| `lei-2021-02292` | Lei nº 2.292, de 9 de novembro de 2021 | 1 | 2021-11-09 to 2021-11-09 |
| `lei-2021-02291` | Lei nº 2.291, de 9 de novembro de 2021 | 1 | 2021-11-09 to 2021-11-09 |
| `lei-2021-02290` | Lei nº 2.290, de 9 de novembro de 2021 | 1 | 2021-11-09 to 2021-11-09 |
| `lei-2021-02289` | Lei nº 2.289, de 9 de novembro de 2021 | 1 | 2021-11-09 to 2021-11-09 |
| `lei-2021-02288` | Lei nº 2.288, de 9 de novembro de 2021 | 1 | 2021-11-09 to 2021-11-09 |
| `lei-2021-02287` | Lei nº 2.287, de 9 de novembro de 2021 | 1 | 2021-11-09 to 2021-11-09 |
| `lei-2021-02286` | Lei nº 2.286, de 9 de novembro de 2021 | 1 | 2021-11-09 to 2021-11-09 |
| `lei-2021-02285` | Lei nº 2.285, de 21 de setembro de 2021 | 1 | 2021-09-21 to 2021-09-21 |

The build made 11 commits:

| Commits | Kind |
| ---: | --- |
| 11 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `futuro`: laws not yet in force on 2026-11-06.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 11 laws in the record.
- 22 tags.

## Dates

Each commit is dated at noon (America/Sao_Paulo) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Decreto-Lei 4.657/1942 (LINDB) art. 1: unless it says otherwise, a law takes effect 45 days after its official publication. This record takes in only municipal laws whose own vigência clause says they take effect on their publication (or signature), and dates each by the publication date the Câmara's SAPL records for it (else by its date). https://www.planalto.gov.br/ccivil_03/decreto-lei/del4657compilado.htm

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `645000404bdd9a072160e8b7017c5fa287c7d507df599108ce53bf97821db3fc` (64722 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `35388bee5aa05369f7da68f5a8fa015ea8d442b8`, `check.py` `5d719354ea4c62d240c93d2cae446307d81d9e81`, `on.py` `aff48cf1b68d50c7ba8f399ca32261871c301824`.
- Python 3.14.4; git version 2.53.0.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Each municipal law ("Lei" and "Lei Complementar") is given as enacted, from the PDF the Câmara's SAPL holds for it, credited to the law itself and dated by the publication date SAPL records for it (else by the law's own date). Later amendments by other laws are not worked into earlier laws: each law is its own file set as enacted. Laws are taken newest first, in parts.
- Left out: scans (with or without an OCR layer), PDFs whose heading does not carry the record's number, texts with no article or no closing date line, texts carrying alteration notes, and laws whose vigência clause sets another day than their publication (or that have none, so that the 45 days of the LINDB apply).
- The text runs from the law's heading to its closing date line (signatures after it are left out); lines repeated at the top or bottom of two or more pages (letterheads, footers) and page numbers are left out. Lines are joined into paragraphs: a new paragraph starts at a provision label, a heading line, or after a line ending in ".", ";" or ":". One file per Art.; "000-titulo" holds what comes before the first article.
- Each municipal law ("Lei" and "Lei Complementar") is given as enacted, from the PDF the Câmara's SAPL holds for it, credited to the law itself and dated by the publication date SAPL records for it (else by the law's own date). Later amendments by other laws are not worked into earlier laws: each law is its own file set as enacted. Laws are taken newest first, in parts.
- Left out: scans (with or without an OCR layer), PDFs whose heading does not carry the record's number, texts with no article or no closing date line, texts carrying alteration notes, and laws whose vigência clause sets another day than their publication (or that have none, so that the 45 days of the LINDB apply).
- The text runs from the law's heading to its closing date line (signatures after it are left out); lines repeated at the top or bottom of two or more pages (letterheads, footers) and page numbers are left out. Lines are joined into paragraphs: a new paragraph starts at a provision label, a heading line, or after a line ending in ".", ";" or ":". One file per Art.; "000-titulo" holds what comes before the first article.
- Each municipal law ("Lei" and "Lei Complementar") is given as enacted, from the PDF the Câmara's SAPL holds for it, credited to the law itself and dated by the publication date SAPL records for it (else by the law's own date). Later amendments by other laws are not worked into earlier laws: each law is its own file set as enacted. Laws are taken newest first, in parts.
- Left out: scans (with or without an OCR layer), PDFs whose heading does not carry the record's number, texts with no article or no closing date line, texts carrying alteration notes, and laws whose vigência clause sets another day than their publication (or that have none, so that the 45 days of the LINDB apply).
- The text runs from the law's heading to its closing date line (signatures after it are left out); lines repeated at the top or bottom of two or more pages (letterheads, footers) and page numbers are left out. Lines are joined into paragraphs: a new paragraph starts at a provision label, a heading line, or after a line ending in ".", ";" or ":". One file per Art.; "000-titulo" holds what comes before the first article.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code (claude-opus-5-5) wrote Lexifina's code and chose the sources. No model output is used as legal text or dates: every word comes from the Câmara's SAPL.
- Claude Code (claude-opus-5-5) wrote Lexifina's code and chose the sources. No model output is used as legal text or dates: every word comes from the Câmara's SAPL.
- Claude Code (claude-opus-5-5) wrote Lexifina's code and chose the sources. No model output is used as legal text or dates: every word comes from the Câmara's SAPL.
