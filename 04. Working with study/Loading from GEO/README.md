This article describes how to prepare a series matrix file from GEO to be loaded to ODM.

# Requirements
* Python 3
* pip
* Having `pandas` library installed. We recommend using the latest version available.
* Genestack Python client installed. See [how to setup Genestack python client](../../00.%20Packages%20to%20install/1.%20Genestack%20python%20client/README.md)
* Auxiliary scripts installed. See [how to install Genestack auxiliary scripts](../../00.%20Packages%20to%20install/2.%20Genestack%20auxiliary%20scripts/README.md)
* Data file from GEO, for example [GSE29746_series_matrix.txt](Example_files/GSE29746_series_matrix.txt)

# Instructions
Run the script providing the `GSE29746_series_matrix.txt` file as an argument

```bash
odm-geo-prepare GSE29746_series_matrix.txt
```

As a result, the script creates the folder with 3 files, that you can use to load to ODM.
For example:

```$ bash
├── GSE17748
│   ├── GSE17748_expression.gct
│   ├── GSE17748_samples.tsv
│   └── GSE17748_study.tsv
```

Load your files to AWS S3 and then to ODM following the [instructions](../../04.%20Working%20with%20study/Uploading%20a%20study/README.md)
