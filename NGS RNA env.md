**Trim-galore incompatible with Python 3.10**

failed when installing trim-galore:

```
(rna) [medkwf4@cas591 ~]$ conda install -c bioconda trim-galore
Collecting package metadata (current_repodata.json): done
Solving environment: failed with initial frozen solve. Retrying with flexible solve.
Solving environment: failed with repodata from current_repodata.json, will retry with next repodata source.

ResolvePackageNotFound:
  - python=3.1
```
Solution:https://stackoverflow.com/questions/71422525/found-conflict-while-installing-packages-with-conda

>1) specify python as an installation target: ```conda install -c conda-forge -c bioconda trim-galore python ```to allow conda to figure out which python version to change your env to
>
>2) Create a new environment specifying what you need from the beginning: ```conda create -n tg -c conda-forge -c bioconda python trim-galore```
