# Python Script for transforming CSV files into ttl against SPARQL query

## Installation

One should perform the following steps before running the script:

1. ``pip install -r requirements.txt``
2. ``git clone https://github.com/Montanaz0r/pytarql.git``
3. cd into cloned repository and run ``pip install .`` to activate setup.py

## Usage

Script can transform in two ways:
1) from csv -> rdf, ``python transform_to_rdf.py [path to input csv] [path to SPARQL query file] [output filename] [version]``
2) from rdf -> csv  ``python transform_to_csv.py [path to rdf file]``

*examples:*    
```python transform_to_rdf.py csv_codelists/glosis_cl.csv example_queries/glosis_cl_example.rq output.ttl 1.1.1```

```python transform_to_csv.py input.ttl output.csv```

Make sure you follow the **camelCase** naming convention when adjusting or adding new records under the attribute column in codelist CSV files. This is very important for the SPARQL query that then transforms the CSV into an RDF representation.
