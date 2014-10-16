# BIOMD0000000064: Teusink2000_Glycolysis

## Installation

Download this repository, and install with distutils

`python setup.py install`

Or, install using pip

`pip install git+https://github.com/biomodels/BIOMD0000000064.git`

To install a specific version (in this example, from the 2014-09-16 BioModels release)

`pip install git+https://github.com/biomodels/BIOMD0000000064.git@20140916`

## Usage

Importing the model package.

`import BIOMD0000000064 as model`

Get the SBML string from the model

`print model.sbmlString`

If [python-libsbml](https://pypi.python.org/pypi/python-libsbml) bindings are
installed, the libsbml.SBMLDocument object is also accessible

`model.sbml`


# Model Notes


**Can yeast glycolysis be understood in terms of in vitro kinetics of the constituent enzymes? Testing biochemistry.**   
_Teusink,B et al.: Eur J Biochem 2000 Sep;267(17):5313-29._  
The model reproduces the steady-state fluxes and metabolite concentrations of
the branched model as given in Table 4 of the paper. It is derived from the
model on JWS online, but has the ATP consumption in the succinate branch with
the same stoichiometrie as in the publication. The model was successfully
tested on copasi v.4.4(build 26).  
For Vmax values, please note that there is a conversion factor of approx. 270
to convert from U/mg-protein as shown in Table 1 of the paper to
mmol/(min*L_cytosol). The equilibrium constant for the ADH reaction in the
paper is given for the reverse reaction (Keq = 1.45*10 4 ). The value used in
this model is for the forward reaction: 1/Keq = 6.9*10 -5 .  
Vmax parameters values used (in [mM/min] except VmGLT):  **VmGLT** | 97.264 |
mmol/min  
---|---|---  
**VmGLK** | 226.45 |   
**VmPGI** | 339.667 |   
**VmPFK** | 182.903 |   
**VmALD** | 322.258 |   
**VmGAPDH_f** | 1184.52 |   
**VmGAPDH_r** | 6549.68 |   
**VmPGK** | 1306.45 |   
**VmPGM** | 2525.81 |   
**VmENO** | 365.806 |   
**VmPYK** | 1088.71 |   
**VmPDC** | 174.194 |   
**VmG3PDH** | 70.15 |   
The result of the G6P steady state concentration (marked in red) differs
slightly from the one given in table 4. of the publication  
Results for steady state:  | orig. article | this model  
---|---|---  
**Fluxes[mM/min]**    |  |   
Glucose  | 88  | 88  
Ethanol  | 129  | 129  
Glycogen  | 6  | 6  
Trehalose  | 4.8  | 4.8  | (G6P flux through trehalose branch)  
Glycerol  | 18.2  | 18.2  
Succinate  | 3.6  | 3.6  
**Conc.[mM]**    |  |   
G6P  | 1.07  | 1.03  
F6P  | 0.11  | 0.11  
F1,6P  | 0.6  | 0.6  
DHAP  | 0.74  | 0.74  
3PGA  | 0.36  | 0.36  
2PGA  | 0.04  | 0.04  
PEP  | 0.07  | 0.07  
PYR  | 8.52  | 8.52  
AcAld  | 0.17  | 0.17  
ATP  | 2.51  | 2.51  
ADP  | 1.29  | 1.29  
AMP  | 0.3  | 0.3  
NAD  | 1.55  | 1.55  
NADH  | 0.04  | 0.04  
Authors of the publication also mentioned a few misprints in the original
article:  
in the kinetic law for _ADH_ :

  1. the species _a_ should denote _NAD_ and _b_ _Ethanol_
  2. the last term in the equation should read _bpq_ /( _K ib K iq K p _ ) 
in the kinetic law for _PFK_ :

  1. R = 1 + λ 1 \+ λ 2 \+ g r λ 1 λ 2
  2. equation L should read: L = L0*(..) 2 *(..) 2 *(..) 2 not L = L0*(..) 2 *(..) 2 *(..) 
To make the model easier to curate, the species _ATP_ , _ADP_ and _AMP_ were
added. These are calculated via assignment rules from the active phosphate
species, _P_ , and the sum of all _AXP_ , _SUM_P_ .

  

To the extent possible under law, all copyright and related or neighbouring
rights to this encoded model have been dedicated to the public domain
worldwide. Please refer to [CC0 Public Domain
Dedication](http://creativecommons.org/publicdomain/zero/1.0/) for more
information.

In summary, you are entitled to use this encoded model in absolutely any
manner you deem suitable, verbatim, or with modification, alone or embedded it
in a larger context, redistribute it, commercially or not, in a restricted way
or not.

  

To cite BioModels Database, please use: [Li C, Donizelli M, Rodriguez N,
Dharuri H, Endler L, Chelliah V, Li L, He E, Henry A, Stefan MI, Snoep JL,
Hucka M, Le Novère N, Laibe C (2010) BioModels Database: An enhanced, curated
and annotated resource for published quantitative kinetic models. BMC Syst
Biol., 4:92.](http://www.ncbi.nlm.nih.gov/pubmed/20587024)


