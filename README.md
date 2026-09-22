# cloudbank-notebooks

This repository contains Jupyter notebooks that use the
XDMoD Data Analytics Framework via the
[`xdmod-data`](https://pypi.org/project/xdmod-data/) 
package. They provide interactive reporting for [CloudBank](https://www.cloudbank.org).

See also the 
[xdmod-notebooks](https://github.com/ubccr/xdmod-notebooks) on which these were based.

## IMPORTANT: XDMoD account and access token

These notebooks connect to and use a remote data source. To do so, you must have an account on 
[ACCESS XDMoD](https://xdmod.access-ci.org). 

Follow instructions provided in the notebooks to acquire an XDMoD access token, then 
authenticate and use the XDMoD data.

## Setup

To run these notebooks on a local machine, follow the instructions
below to set up the machine to run the notebooks in JupyterLab using e.g.
Anaconda. 

### Anaconda install and use

1. Install Anaconda following [these instructions](https://docs.anaconda.com/free/anaconda/install/index.html).
1. Launch JupyterLab (NOT Jupyter Notebook).
1. Navigate to the notebooks using the Jupyter Lab UI in the browser.

### Download notebooks

The contents of this repository can be downloaded from
the [cloudbank-notebooks page](https://github.com/cloudbank-project/cloudbank-notebooks). 

## License

The notebooks in this repository are based upon the
[xdmod-notebooks](https://github.com/ubccr/xdmod-notebooks). These were
released under
the GNU Lesser General
Public License ("LGPL") Version 3.0. See the xdmod-notebooks LICENSE file for
details.

## References

* [`xdmod-notebooks`](https://github.com/ubccr/xdmod-notebooks)
* [`xdmod-data`](https://pypi.org/project/xdmod-data/) 

These notebooks are possible thanks to the 
Data Analytics Framework for XDMoD:

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
