# cloudbank-notebooks

This repository contains Jupyter notebooks that use the
XDMoD Data Analytics Framework via the
[`xdmod-data`](https://pypi.org/project/xdmod-data/) 
package. They provide interactive reporting for [CloudBank](https://www.cloudbank.org).

See also the 
[xdmod-notebooks](https://github.com/ubccr/xdmod-notebooks) on which these were based.

## IMPORTANT: XDMoD access token

These notebooks connect to and use a remote data source. 
Follow these instructions to acquire an XDMoD access token so you can
authenticate and use the remote XDMoD data warehouse:

1. Confirm you have an account on [ACCESS XDMoD](https://xdmod.access-ci.org). 
1. Log in to ACCESS XDMoD and generate an API token on the XDMoD portal according to [API Token
Access](https://github.com/ubccr/xdmod-data#api-token-access).
1. Save your unique API token to a plain text file on your local machine, for
example, `~/xdmod-data.env`. The contents must be: `XDMOD_API_TOKEN=my_token`. This file should be
saved with `600` permissions (user read/write only) and must be accessible to the Jupyter
environment.
1. Inside the notebook, load your access token using the following syntax:

```
from dotenv import load_dotenv
from os.path import expanduser
from pathlib import Path

load_dotenv(Path(expanduser('~/xdmod-data.env')), 
            override=True)
```

### Set URL in the DataWarehouse object

For production access from your local machine, 
provide the URL of the XDMoD portal 
(`https://xdmod.access-ci.org`)
to the DataWarehouse constructor.
Do this inside your notebook:

```
from xdmod_data.warehouse import DataWarehouse
dw = DataWarehouse("https://xdmod.access-ci.org")
```

Alternately you may set the URL in the `XDMOD_HOST` environment variable in your notebook as follows:
```
import os
os.environ["XDMOD_HOST"] = "https://xdmod.access-ci.org"
```

These steps will enable your notebooks to access the production XDMoD data warehouse.

## Setup

To run these notebooks on a local machine, clone this repo locally, then follow the instructions
below to set up JupyterLab using e.g. Anaconda. 

### Download notebooks

The contents of this repository can be downloaded from
the [cloudbank-notebooks page](https://github.com/cloudbank-project/cloudbank-notebooks). 

### Anaconda installation and use

1. Install Anaconda following [these instructions](https://docs.anaconda.com/free/anaconda/install/index.html).
1. Launch Jupyter Lab (NOT Jupyter Notebook).
1. Navigate to the notebooks using the Jupyter Lab UI in the browser.

## License

The notebooks in this repository are based upon the
[xdmod-notebooks](https://github.com/ubccr/xdmod-notebooks). These were
released under the GNU Lesser General
Public License ("LGPL") Version 3.0. See the xdmod-notebooks LICENSE file for
details.

## References

* [`xdmod-notebooks`](https://github.com/ubccr/xdmod-notebooks)
* [`xdmod-data`](https://pypi.org/project/xdmod-data/) 

These notebooks are possible thanks to the Data Analytics Framework for XDMoD:

> Weeden, A., White, J.P., DeLeon, R.L., Rathsam, R., Simakov, N.A., Saeli, C.,
> and Furlani, T.R. The Data Analytics Framework for XDMoD. _SN COMPUT. SCI._
> 5, 462 (2024). 
> DOI: [10.1007/s42979-024-02789-2](https://doi.org/10.1007/s42979-024-02789-2)

See also ACCESS XDMoD:

> Jeffrey T. Palmer, Steven M. Gallo, Thomas R. Furlani, Matthew D. Jones,
> Robert L. DeLeon, Joseph P. White, Nikolay Simakov, Abani K. Patra, Jeanette
> Sperhac, Thomas Yearke, Ryan Rathsam, Martins Innus, Cynthia D. Cornelius,
> James C. Browne, William L. Barth, Richard T. Evans, "Open XDMoD: A Tool for
> the Comprehensive Management of High-Performance Computing Resources",
> *Computing in Science & Engineering*, Vol 17, Issue 4, 2015, pp. 52-62.
> DOI: [10.1109/MCSE.2015.68](https://doi.org/10.1109/MCSE.2015.68)
