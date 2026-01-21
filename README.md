# T6SS orthologs 2026

A Python tool for querying the NCBI Clusters of Orthologous Genes (COG) database to identify bacterial species with Type VI Secretion System (T6SS) gene sets.

## Overview

This tool searches the NCBI COG database for 14 core T6SS components and identifies species that possess the complete gene set. For each T6SS gene, it retrieves:

- COG identifier and metadata
- PDB structural entries
- Orthologous genes across all bacterial genomes

## T6SS Genes Searched

| Gene | COG ID |
|------|--------|
| tssA | COG3515 |
| tssB | COG3516 |
| tssC | COG3517 |
| tssD | COG3157 |
| tssE | COG3518 |
| tssF | COG3519 |
| tssG | COG3520 |
| tssH | COG0542 |
| tssI | COG3501 |
| tssJ | COG3521 |
| tssK | COG3522 |
| tssL | COG3455 |
| tssM | COG3523 |
| PAAR | COG4104 |

## Repository Contents

- `t6ss_cog_search.ipynb` - Jupyter notebook to run the search
- `t6ss_complete_species.csv` - Full results table (generated January 20, 2026)
- `README.md` - This file

## Output

The tool generates a CSV with the following structure:

| T6SS_gene | PDB_entries | COG_ID | Species_1 | Species_2 | ... |
|-----------|-------------|--------|-----------|-----------|-----|
| tssA | 6GIY | COG3515 | gene_tag | gene_tag | ... |
| tssB | 3ZRJ | COG3516 | gene_tag | gene_tag | ... |
| ... | ... | ... | ... | ... | ... |

Only species with all 14 T6SS genes are included in the output.

## Associated Publication

[Link to paper]

## References

- NCBI COG Database: https://www.ncbi.nlm.nih.gov/research/cog/
- COG API Documentation: https://www.ncbi.nlm.nih.gov/research/cog/webservices/

## License

MIT License
