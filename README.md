# PyFMGUI

## Introduction
PyFMGUI is an application for the analysis of force microscopy data capable of analyzing Nanoscope and JPK AFM files.

The following analysis routines are supported:
- Thermal tune calibration (JPK .tnd files)
- Elastic fit (Hertz Model fit)
- Viscoelastic fit
- Piezo characterization
- Viscous drag correction
- Microrheology (DMA) analysis

If you have any suggestions, comments or experience any issues. Please open an issue on this repository 
https://github.com/jlopezalo/PyFMGUI/issues

or write to us @ yogesh.saravanan@inserm.fr

## Run software
A zip containing the frozen application can be found and downloaded here:

[https://doi.org/10.5281/zenodo.8301684](https://zenodo.org/records/8342163)

To run, extract the contents of the .zip and run the main.exe file.

## To run from source
- Clone the repository
```
git clone  https://github.com/DyNaMo-INSERM/PyFMGUI_DyNaMo.git
cd ./PyFMGUI
```
- Create an environment with python 3.9
```
conda create -n yourenvname python=3.9 
conda activate yourenvname
```

- Install the dependencies from requirements.txt
```
pip install -r requirements.txt
```
- Install the PYFMreader and PyFMRheo from DyNaMo's repositary
```

pip install -e git+https://github.com/DyNaMo-INSERM/PyFMReader_DyNaMo@master#egg=pyfmreader_dynamo    

pip install -e git+https://github.com/DyNaMo-INSERM/PyFMRheo_DyNaMo@main#egg=pyfmrheo_dynamo

```

- run src/main.py
```
python src/main.py
```

## Generate executables
If you wish to do any changes to the code and freeze them. You can use PyInstaller and run the main.spec file (Windows).
```
python -m PyInstaller main.spec
```

## To Do
- Generate documentation with examples and tutorials
- Improve multiprocessing
- Improve tree control for files (allow to load multiple directories at once and assign folder as group)
- Allow to save analysis sessions and load them after
- Improve error handling and logging

## Acknowledgements
This project has received funding by the H2020 European Union’s Horizon 2020 research and innovation program under the Marie Sklodowska-Curie (grant agreement No 812772) and from the European Research Council (ERC, grant agreement No 772257).

