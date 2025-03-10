# Table of contents

- [Table of contents](#table-of-contents)
- [Info](#info)
- [Documentation](#documentation)
- [Meta-data](#meta-data)
- [Tools](#tools)
  - [Transformer-tool](#transformer-tool)
    - [Installation](#installation)
    - [Usage](#usage)
  - [Version Updater](#version-updater)
    - [Requirements](#requirements)
    - [Usage](#usage-1)
- [Contribution](#contribution)
- [Citing](#citing)


# Info

This repository contains the Global Soil Information System (GloSIS) v1.0 ontology network, derived from the source UML data model,
and modelled in line with best practices and methodologies, reusing existing standard models and ontologies.

# Documentation

All modules in this web ontology are documented individually with HTML pages
generated with the [WiDoco](https://github.com/dgarijo/Widoco) tool. These pages can be accessed at [https://glosis-ld.github.io/glosis/docs/](https://glosis-ld.github.io/glosis/).

Configuration files for WiDoco are generated automatically with a [bespoke
tool](https://github.com/glosis-ld/glosis/blob/master/docs/README_WiDoco.md).
Documentation pages are maintained in the [docs folder](https://github.com/glosis-ld/glosis/blob/master/docs).

The documentation for each module can be accessed via the [documentation entry page](https://glosis-ld.github.io/glosis/).

# Meta-data

Besides the meta-data encoded in RDF with the ontology itself, there is also a
meta-data record for GloSIS at the
[FAIRSharing.org](https://fairsharing.org/5073) catalogue. The DOI of this
record is
[https://doi.org/10.25504/FAIRsharing.af87a1](https://doi.org/10.25504/FAIRsharing.af87a1) 

# Tools

## Transformer-tool

[Transformer-tool](https://github.com/glosis-ld/glosis/tree/master/utils/transformer_tool) is a bi-directional tool that allows generating RDF representation using SPARQL query and list of codelist items in CSV file or another way around by generating a CSV list of items out of RDF representation.

### Installation

One should perform the following steps before running the script:

1. ``pip install - r requirements.txt``
2. ``git clone https://github.com/Montanaz0r/pytarql.git``
3. cd into cloned repository and run ``pip install .`` to activate setup.py

### Usage

Script can transform in two ways:
1) from csv -> rdf, ``python transform_to_rdf.py [path to input csv] [path to SPARQL query file] [output filename] [version]``
2) from rdf -> csv  ``python transform_to_csv.py [path to rdf file]``

*examples:*    
```python transform_to_rdf.py data/test.csv data/myquery.rq output.ttl 1.1.1```

```python transform_to_csv.py input.ttl```
(this creates a csv file with corresponding filename in the location of TURTLE file)

read more about the transformer-tool [HERE](https://github.com/glosis-ld/glosis/wiki/UTILITY:-Transformer-Tool).

## Version Updater

[Version updater](https://github.com/glosis-ld/glosis/tree/master/utils/version_updater) is a simple convenience script that updates and harmonizes versions across all ontology modules.

### Requirements

python3

### Usage

*example:*    
```python utils/version_updater/version_updater.py 3.0.1```

# Contribution

One can find the current list of code lists provided as CSV files under the *csv_codelists* directory. Those code lists can be used as input to modify the ontology using the [Transformer-tool](#transformer-tool). CI/CD pipeline is taking care of maintaining the current version of code lists. That means one needs to push modifications onlt via TURTLE files and don't need to worry about updating CSV code lists alongside.

# Acknowledgment

The work in this paper has been supported by and partially carried out in the
scope of the SIEUSOIL and EJP SOIL projects and by ISRIC – World Soil
Information. EJP SOIL and SIEUSOIL has received funding from the European
Union’s Horizon 2020 research and innovation programme. The EJP SOIL Grant
agreement No is 862695, the SIEUSOIL Grant agreement No is 818346. ISRIC – World
Soil Information supports the soil community with soil, soil data, soil data
exchange standard development to support soil data, information and knowledge
provisioning at global, national and sub-national levels for application into
sustainable management of soil and land.

# Citing

Cite as:

> Palma R., Janiak B., Reznik T., Schleidt K., Kozel, J., De Sousa L., Egmond F., Mouazen A. M., Moshou, D. (2020) Global Soil Information System (GloSIS) Ontology. SIEUSOIL project. http://w3id.org/glosis/model 


Shield: [![CC BY NC SA 3.0 IGO][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 3.0 IGO][cc-by].

[![CC BY NC SA 3.0 IGO][cc-by-image]][cc-by]

[cc-by]: https://creativecommons.org/licenses/by-nc-sa/3.0/igo/
[cc-by-image]: https://licensebuttons.net/l/by/3.0/igo/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%20NC%20SA%203.0%20IGO-lightgrey.svg
