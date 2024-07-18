# nublado-seeds

This repository contains a hierarchy of directories, each pertaining to a particular service for which a user might want to generate a templated notebook via [times-square](https://times-square.lsst.io/).  Each directory contains multiple pairs of files.  Each pair contains one `.ipynb` JSON document that is a test notebook, and a corresponding `.yaml` file containing metadata and parameterization characterization for that notebook.

## portal

These are templated notebooks that talk to the Firefly implementation that is the Portal Aspect of the RSP.

### query

[query.ipynb](portal/query.ipynb) takes a single parameter, `query_url` (which a user would get via doing a search in the Portal, choosing the Info button, and copying the query URL show there).
It then retrieves that query from the Portal, and follows its result chain in order to render the query results into a pandas DataFrame.
Finally it displays a preview of that DataFrame.
