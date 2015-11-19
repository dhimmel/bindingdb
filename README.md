# Processing BindingDB

[![DOI](https://zenodo.org/badge/14475/dhimmel/bindingdb.svg)](https://zenodo.org/badge/latestdoi/14475/dhimmel/bindingdb)

This repository contains our processing of [BindingDB](https://www.bindingdb.org/bind/index.jsp). Refer to the corresponding [Thinklab discussion](https://doi.org/10.15363/thinklab.d53) for more information.

## License

BindingDB includes the following [licensing statement](https://github.com/dhimmel/integrate/blob/1a43ef2718283cbfc9ae869aee1856bf20e2ad6e/licenses/custom/BindingDB.md):

> Data imported from ChEMBL are provided under their [Creative Commons Attribution-Share Alike 3.0 Unported License](https://www.ebi.ac.uk/chembl/about). All data curated by BindingDB staff are provided under the [Creative Commons Attribution 3.0 License](https://creativecommons.org/licenses/by/3.0/us/).

All original content in this repository is released as [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

## Execution

The analysis can be reproduced by running `process.ipynb` followed by `collapse.Rmd`.

The python notebook `process.ipynb`:

+ processes affinities to floats
+ converts to entrez genes
+ simplifies observations into essential fields

The rmarkdown script `collapse.Rmd`:

+ filters to human experiments
+ converts to drugbank compounds
+ collapses observations by compound-gene pairs
