# RF-PUB-10 Submission Transport Manifest

Date: 2026-05-24 UTC

Program: resonance-physics

Branch: formal-resonance-taxonomy

Purpose: local submission package for the PRA RevTeX formal-resonance-taxonomy manuscript after the RF-PUB-09 pre-journal-submission patches and the RF-PUB-13 claim/ledger repair.

## Packet State

Status: LOCAL_PACKAGE_READY_WITH_54_CASE_SUPPLEMENT_AND_5_MODEL_COUNCIL_PASS

Recovery source: `/data/research/hive_brain_lv9ss6qn/stdout.json`

The original RF-PUB-10 package directory was absent on 2026-05-21. This manifest rematerializes the package from the preserved RF-PUB-10 leader session transcript, then rebuilds and fresh-extraction compile-smokes it in the current workspace. RF-PUB-13 adds the public 54-case-test supplement and claim-count guard so the manuscript no longer down-scopes the adjudicated 54-case result to the representative printed 15-row appendix.

## Patch Ledger Resolved

1. Author metadata is set to `Old\v{r}ich Dvo\v{r}\'ak`, affiliation `Independent researcher`, email `oldrich@oldrich.me`.
2. Raw numeric citation references in the manuscript body are converted to keyed `\cite{}` calls backed by a dedicated BibTeX database.
3. The manuscript claim now states `54 documented case-tests` and treats the printed 15-row appendix as representative only.
4. The arXiv source directory includes `2026-05-24_RF-PUB-13_54_case_public_supplement.tsv`.
5. `/opt/hive/scripts/research-publication-claim-guard.py` passes for both the manuscript source and the arXiv source copy with `--expected-count 54`.
6. RF-PUB-13 release council passed across Codex high, Gemini Pro, Deepseek V4 Flash, Deepseek V4 Pro, and Claude Opus on 2026-05-24.

## Files

| Role | File | SHA-256 |
|---|---|---|
| PRA RevTeX source | `2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.tex` | `301328c57c45216cda9b1f767f4e5b6dc297f814678003c1dbb6311ddbbc2912` |
| BibTeX database | `2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex_refs.bib` | `5f7714b4f46bfe728cedd4712ad23c5f5c8b3a911b0e9b6fb22edd2d2aaa28fe` |
| Public 54-case supplement | `2026-05-24_RF-PUB-13_54_case_public_supplement.tsv` | `71a0d3c6e29966fc7f5fd89a3da61b4b969fdbb62e79993c49ef2735dc1d3441` |
| Compiled PDF | `2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.pdf` | `005ccde92dc78a735107bf8d5ead8deada487d167f6d8d45cc3521e5e107e684` |
| Main build log | `2026-05-20_RF-PUB-10_build_log.txt` | `8af731b8e20ffc7022b84a68abce6863c55eab5b39858c9497d767b5e72a0936` |
| Generated BBL | `2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.bbl` | `0f518fb50bdd80457ed8b0e431eb61915b697333d79676aa7e48b2734575748c` |
| arXiv source tarball | `2026-05-20_RF-PUB-10_arxiv_source.tar.gz` | `78d079733ad240c2356425b0a3153b7fa7ec19f40e3f340c3280ca88969a7c43` |
| Fresh-extraction compile log | `2026-05-20_RF-PUB-10_arxiv_package_compile_log.txt` | `f6e300fb735b39038c0de23ed1a4c9d636937e1331bc97c24e1b417bb5d4ac9c` |

## Compile Smoke

Command:

```bash
cd /data/research/programs/resonance-physics/publication_inputs
/tmp/tectonic-0.16.9/musl/tectonic --keep-logs --keep-intermediates 2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.tex
```

Result: `PASS`

Fresh extraction command:

```bash
tar -xzf /data/research/programs/resonance-physics/publication_inputs/2026-05-20_RF-PUB-10_arxiv_source.tar.gz
cd 2026-05-20_RF-PUB-10_arxiv_source
/tmp/tectonic-0.16.9/musl/tectonic --keep-logs --keep-intermediates main.tex
```

Result: `PASS`

The compile logs contain only non-blocking typography/style diagnostics. No undefined citations, missing bibliography entries, raw numeric citation brackets in source, emergency stops, LaTeX errors, or missing database-entry failures were found by the recovery validation.

## Claim/Ledger Guard

Command:

```bash
python3 /opt/hive/scripts/research-publication-claim-guard.py \
  --paper /data/research/programs/resonance-physics/publication_inputs/2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.tex \
  --ledger /data/research/programs/resonance-physics/publication_inputs/2026-05-24_RF-PUB-13_54_case_public_supplement.tsv \
  --expected-count 54
```

Result: `PASS` (`ledger_rows=54`; manuscript claim numbers include `54`, with `15` only as a representative subset).

## RF-PUB-13 Council

Result: `PASS`

Council lanes:

- Codex high: `PASS`
- Gemini Pro: `PASS`
- Deepseek V4 Flash: `PASS`
- Deepseek V4 Pro: `PASS`
- Claude Opus: `PASS` after retry with artifacts copied into the Claude sandbox

Council scope: 54-vs-15 claim integrity, supplement sufficiency, bounded no-fifth-family wording, and publication guard wiring. Non-blocking Opus hardening note was applied immediately: the claim guard now requires local qualification near smaller-count mentions instead of accepting a global `representative` occurrence elsewhere in the paper.

## Claim Boundary

This is an artifact recovery and transport-readiness restoration plus claim/ledger repair. It does not add resonance science, taxonomy families, guardrail wording, or instrument claims; it restores the adjudicated 54-case-test publication surface and prevents accidental down-scoping to the representative 15-row appendix.

## Remaining External Blockers

Live arXiv/Zenodo transport remains blocked until authenticated publication credentials/session are available. GitHub transport has been updated in `oldrich-research/formal-resonance-taxonomy` with the 54-case supplement. Local git is present in the 2026-05-21 runtime and should not be listed as a current local blocker.
