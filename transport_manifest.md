# RF-PUB-10 Submission Transport Manifest

Date: 2026-05-20 UTC

Program: resonance-physics

Branch: formal-resonance-taxonomy

Purpose: local submission package for the PRA RevTeX formal-resonance-taxonomy manuscript after the RF-PUB-09 pre-journal-submission patches.

## Packet State

Status: LOCAL_PACKAGE_READY_RESTORED_FROM_SESSION_TRANSCRIPT

Recovery source: `/data/research/hive_brain_lv9ss6qn/stdout.json`

The original RF-PUB-10 package directory was absent on 2026-05-21. This manifest rematerializes the package from the preserved RF-PUB-10 leader session transcript, then rebuilds and fresh-extraction compile-smokes it in the current workspace.

## Patch Ledger Resolved

1. Author metadata is set to `Old\v{r}ich Dvo\v{r}\'ak`, affiliation `Independent researcher`, email `oldrich@oldrich.me`.
2. Raw numeric citation references in the manuscript body are converted to keyed `\cite{}` calls backed by a dedicated BibTeX database.

## Files

| Role | File | SHA-256 |
|---|---|---|
| PRA RevTeX source | `2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.tex` | `13c3f64601241b4a190a37c25984df1ebb4370ea17a65caf637a3dea0163fec3` |
| BibTeX database | `2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex_refs.bib` | `2c6e19f782311abbef4ae5031ea0595b8786b45b5c21211d84d9e0ed978c045c` |
| Compiled PDF | `2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.pdf` | `46198b421361c44520d64cd6ec1e847f385519aed0c2712add7b1afb5426f0bd` |
| Main build log | `2026-05-20_RF-PUB-10_build_log.txt` | `8af731b8e20ffc7022b84a68abce6863c55eab5b39858c9497d767b5e72a0936` |
| Generated BBL | `2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.bbl` | `c043921cf98bcbe22ac12173e01f53cd1c2d9dcb749990452961633f28ffb8c6` |
| arXiv source tarball | `2026-05-20_RF-PUB-10_arxiv_source.tar.gz` | `f620ed44f5ebcb737006aa56ce43f99590a11f1c804381d1e5ec06e2d57236f2` |
| Fresh-extraction compile log | `2026-05-20_RF-PUB-10_arxiv_package_compile_log.txt` | `f6e300fb735b39038c0de23ed1a4c9d636937e1331bc97c24e1b417bb5d4ac9c` |

## Compile Smoke

Command:

```bash
cd /data/research/programs/resonance-physics/publication_inputs
/tmp/tectonic-rfpub10/tectonic --keep-logs --keep-intermediates 2026-05-16_RF-PUB-08_formal_resonance_taxonomy_pra_revtex.tex
```

Result: `PASS`

Fresh extraction command:

```bash
tar -xzf /data/research/programs/resonance-physics/publication_inputs/2026-05-20_RF-PUB-10_arxiv_source.tar.gz
cd 2026-05-20_RF-PUB-10_arxiv_source
/tmp/tectonic-rfpub10/tectonic --keep-logs --keep-intermediates main.tex
```

Result: `PASS`

The compile logs contain only non-blocking typography/style diagnostics. No undefined citations, missing bibliography entries, raw numeric citation brackets in source, emergency stops, LaTeX errors, or missing database-entry failures were found by the recovery validation.

## Claim Boundary

This is an artifact recovery and transport-readiness restoration only. It does not add resonance science, taxonomy families, guardrail wording, or instrument claims.

## Remaining External Blockers

Live arXiv/GitHub/Zenodo transport remains blocked until authenticated publication credentials/session are available. Local git is present in the 2026-05-21 runtime and should not be listed as a current local blocker.
