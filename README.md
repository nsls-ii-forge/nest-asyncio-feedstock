About nest-asyncio
==================

Home: https://github.com/erdewit/nest_asyncio

Package license: BSD-2-Clause

Feedstock license: BSD-3-Clause

Summary: Patch asyncio to allow nested event loops

By design asyncio does not allow its event loop to be nested.
This presents a practical problem - when in an environment where the event loop is already running it's impossible to run tasks and wait for the result.
Trying to do so will give the error RuntimeError - This event loop is already running.
The issue pops up in various environments, such as web servers, GUI applications and in Jupyter notebooks.
This module patches asyncio to allow nested use of asyncio.run and loop.run_until_complete.


Current build status
====================


<table><tr><td>All platforms:</td>
    <td>
      <a href="https://dev.azure.com/nsls2forge/nsls2forge/_build/latest?definitionId=241&branchName=master">
        <img src="https://dev.azure.com/nsls2forge/nsls2forge/_apis/build/status/nest-asyncio-feedstock?branchName=master">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-nest--asyncio-green.svg)](https://anaconda.org/nsls2forge/nest-asyncio) | [![Conda Downloads](https://img.shields.io/conda/dn/nsls2forge/nest-asyncio.svg)](https://anaconda.org/nsls2forge/nest-asyncio) | [![Conda Version](https://img.shields.io/conda/vn/nsls2forge/nest-asyncio.svg)](https://anaconda.org/nsls2forge/nest-asyncio) | [![Conda Platforms](https://img.shields.io/conda/pn/nsls2forge/nest-asyncio.svg)](https://anaconda.org/nsls2forge/nest-asyncio) |

Installing nest-asyncio
=======================

Installing `nest-asyncio` from the `nsls2forge` channel can be achieved by adding `nsls2forge` to your channels with:

```
conda config --add channels nsls2forge
```

Once the `nsls2forge` channel has been enabled, `nest-asyncio` can be installed with:

```
conda install nest-asyncio
```

It is possible to list all of the versions of `nest-asyncio` available on your platform with:

```
conda search nest-asyncio --channel nsls2forge
```




Updating nest-asyncio-feedstock
===============================

If you would like to improve the nest-asyncio recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`nsls2forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `nsls2forge` channel.
Note that all branches in the nsls-ii-forge/nest-asyncio-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@yehoshuadimarsky](https://github.com/yehoshuadimarsky/)

