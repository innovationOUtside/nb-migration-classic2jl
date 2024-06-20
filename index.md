# Jupyter notebook migration guide

Whilst there should be minimal disruption to code execution when moving from Jupyter's _classic notebook_ user interface to the JupyterLab / notebook v7, _except in cases where magics are being used that relied on front end interface code calls to work their magic_, there are two main areas where updates will or may be required:

- classic notebook extensions will not work in the JupyterLab/nb7 environment and **will** need updating
- notebooks that have cell tags or metadata set by previous extensions to modify cell presentation or behaviour _may_ meed modifying

Please feel free to post an issue [here](https://github.com/innovationOUtside/nb-migration-classic2jl/issues) describing any notebook migration issues you encounter for which mitigation or a solution has not been described.
