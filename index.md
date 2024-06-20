# Jupyter notebook migration guide

Whilst there should be minimal disruption to code execution when moving from Jupyter's _classic notebook_ user interface to the JupyterLab / notebook v7, _except in cases where magics are being used that relied on front end interface code calls to work their magic_, there are two main areas where updates will or may be required:

- classic notebook extensions will not work in the JupyterLab/nb7 environment and **will** need updating
- notebooks that have cell tags or metadata set by previous extensions to modify cell presentation or behaviour _may_ meed modifying

Please feel free to post an issue [here](https://github.com/innovationOUtside/nb-migration-classic2jl/issues) describing any notebook migration issues you encounter for which mitigation or a solution has not been described.

*For a complete description of extensions used in the TM351 VCE, as well as the installer pack used to install all the extensions, and recommended default settings for user-isntalled and core JupyterLab / nmbv7 extensions, see [here](https://innovationoutside.github.io/ou-tm351-jl-extensions/).*

Extension update guide:

| Extension | ClassicNb Extension name | JL/nb7 Extension name | Notes |
| ------------- | ------------- |  ------------- | ------------- | 
| Empinken  | [`nb_extension_empinken`](https://github.com/innovationOUtside/nb_extension_empinken) |[`jupyterlab_empinken_extension`](https://github.com/innovationOUtside/jupyterlab_empinken_extension) | Just update package name |
| Cell execution status  | [`nb_cell_execution_status`](https://github.com/innovationOUtside/nb_cell_execution_status/) | [`jupyterlab_cell_status_extension`](https://github.com/innovationOUtside/jupyterlab_cell_status_extension)| Just update package name |
| Spellchecker | [`nbextensions/spellchecker`](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions/spellchecker/README.html)|[`jupyterlab-contrib/spellchecker`](https://github.com/jupyterlab-contrib/spellchecker)|Just update package name |
|Download zip archive|[`nbzip`](https://github.com/data-8/nbzip)|[`jupyter-archive`](https://github.com/jupyterlab-contrib/jupyter-archive)|Just update package name|
|Skip traceback| [nbextensions/skip-traceback](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions/skip-traceback/readme.html)|[`jupyterlab-skip-traceback`](https://github.com/deshaw/jupyterlab-skip-traceback)| Update package name; [update settings](https://innovationoutside.github.io/ou-tm351-jl-extensions/settings-skip-traceback.html) to show folded trace by default|
|Collapsible headings|[`nbextensions/collapsible_headings`](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions/collapsible_headings/readme.html)|*Native in JL4/nb7*||
|Table of contents|[`nbextensions/toc2`](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions/toc2/README.html)|*Native in JL4/nb7*||

JupyterLab OU branding extension (pending updates to core VCE): [`innovationOUtside/jupyterlab-ou-brand-extension`](https://github.com/innovationOUtside/jupyterlab_ou_brand_extension/)

Tag / metadata update:

|Feature| Classic nb tag / metadata | JL / Nb7 tag / metadata|Notes|
| ------------- | ------------- |  ------------- | ------------- | 
| Collapsible headings|Metadata (collapsed header): `heading_collapsed: true`|Metadata (collapsed header): `"jp-MarkdownHeadingCollapsed": true` | Optional 'hidden' metadata in collapsed hidden cells can be removed.|

A command line tool to update notebook cell tag/metadata will be available here by Weds 26/6/24 at the latest.
