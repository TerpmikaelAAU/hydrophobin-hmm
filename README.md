# hydrophobin-hmm

Identification and class I / class II assignment of hydrophobins in the *Apiospora arundinis*
proteome, using profile HMMs built from characterised reference hydrophobins.

## Contents

| | |
|---|---|
| `hydrophobins.ipynb` | the analysis |
| `data/hydrophobin_references.fasta` | 21 characterised hydrophobins (10 class I, 11 class II) with NCBI/UniProt accessions |
| `data/hydrophobin_names.tsv` | name and locus tag for each hit |
| `data/protein.faa` | *A. arundinis* predicted proteome (15,721 proteins) |

## Result

| Name | Gene | Accession | Class | E-value | Pfam |
|---|---|---|---|---|---|
| AaHyd1 | PGQ11_000491 | KAK8879197.1 | I | 3.2e-05 | no hit |
| AaHyd2 | PGQ11_012533 | KAK8856621.1 | I | 4.0e-18 | PF01185 |
| AaHyd3 | PGQ11_000931 | KAK8879637.1 | II | 1.3e-37 | PF06766 |
| AaHyd4 | PGQ11_004185 | KAK8873671.1 | II | 3.9e-34 | PF06766 |
| AaHyd5 | PGQ11_005659 | KAK8875145.1 | II | 6.5e-28 | PF06766 |
| AaHyd6 | PGQ11_012458 | KAK8856546.1 | II | 7.8e-11 | PF06766 |

Names (class, then locus tag) are fixed in `data/hydrophobin_names.tsv`; the notebook stops if a
hit is missing from it.

## Running

Requires Python ≥ 3.10 and [IQ-TREE 2](https://github.com/iqtree/iqtree2/releases) on `PATH`
(or in `tools/`).

```bash
pip install -r requirements.txt
jupyter lab hydrophobins.ipynb
```

Outputs are written to `results/`.

## License

MIT
