# GEO Disease Expression Analysis

A Jupyter notebook for comparing gene expression between Normal and Disease samples in NCBI GEO microarray and bulk RNA-seq datasets.

## Usage

```bash
pip install -r requirements.txt
jupyter notebook geo_normal_disease_analysis.ipynb
```

Set `GSE_ID` and `GENE_ID` in the first cell. Age and sex adjustment is optional and disabled by default.

Group labels are inferred from GEO metadata when possible. Review the generated audit files before interpreting results.

## Validation and limitations

This notebook supports **exploratory comparisons of one specified gene** between groups derived from GEO samples.

- Automatically inferred Normal / Disease labels are heuristic. Review the exported audit CSV and manually correct or exclude samples when needed.
- Do not combine distinct diseases, tissues, treatments, or collection conditions without a scientifically justified comparison definition.
- Verify expression units, preprocessing, sample sizes, and the gene / platform mapping. Different GSE records may require configuration changes or a locally supplied expression matrix.
- Optional age and sex covariates do not resolve all confounding, selection bias, or differences in the underlying study design.
- Results should not be interpreted as diagnostic performance, causality, or confirmation of disease-associated gene expression.
- Exploratory analysis of RNA-seq expression measurements is not a replacement for a properly designed count-based differential-expression workflow.
- This repository does not currently publish a systematic list of independently validated GSE studies or benchmark results.

## Reproducibility checklist

1. Record GSE accession, NCBI Gene ID, expression source, inclusion filters and covariate settings.
2. Install dependencies from `requirements.txt`; set `GSE_ID` and `GENE_ID` in the notebook.
3. Verify group assignments from the exported audit files; document all overrides and exclusions.
4. Inspect the comparison outputs and original GEO metadata before reporting findings.

The notebook and dependency list are public. Results depend on the available GEO annotations and the selected study conditions.
