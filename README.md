# GEO Disease Expression Analysis

A Jupyter notebook for comparing gene expression between Normal and Disease samples in NCBI GEO microarray and bulk RNA-seq datasets.

## Usage

```bash
pip install -r requirements.txt
jupyter notebook geo_normal_disease_analysis.ipynb
```

Set `GSE_ID` and `GENE_ID` in the first cell. Age and sex adjustment is optional and disabled by default.

Group labels are inferred from GEO metadata when possible. Review the generated audit files before interpreting results.
