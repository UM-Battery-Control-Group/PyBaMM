# Code for modeling battery degradation and expansion

If you use this model in your work, please cite out paper
S. Pannala,H. Movahedi, T.R. Garrick, J.B. Siegel, and A. Stefanopoulou, "Consistently Tuned Battery Lifetime Predictive Model of Capacity Loss, Resistance Increase, and Irreversible Thickness Growth", Journal of The Electrochemical Society, 171(1), 010532. 
DOI: [https://doi.org/10.1149/1945-7111/ad1294](https://doi.org/10.1149/1945-7111/ad1294)

## Installation instructions
1. Install [git](https://git-scm.com/downloads) 
2. Install [python 3.9](https://www.python.org/downloads/release/python-3913/)
3. Clone the git repo and change directory to the PyBaMM folder:
```
git clone https://github.com/UM-Battery-Control-Group/PyBaMM
cd PyBaMM
```

4. Ensure that you are in the PyBaMM working directory. Switch to the `deg-model-pub` branch of the PyBaMM fork
```
git checkout deg-model-pub
```
5. Follow install from source instruction from PyBaMM documentation to install our custom fork of PyBaMM
https://docs.pybamm.org/en/v23.1/source/user_guide/installation/install-from-source.html

6. Change the working directory to `degradation_model` subfolder
```
cd degradation_model
```
## Data
The model requires cycling data, RPT data, resistance and eSOH data. These data files not included in this repo due to upload size limitations. Please download from this [Google Drive Folder](https://drive.google.com/drive/folders/19DtSIYLwB66Q97tN5NyM95HA_uPVLkRg?usp=drive_link) and paste the files in the empty folder named `data` provided. Ensure to paste the data in the corresponding subfolders of `cycling`,`esoh`,`ocv`, `hppc` and `resistance`.
## Running the Model
- Run [run_model.ipynb](./degradation_model/run_model.ipynb) notebook to simulate aging for all cells at room temperature
  - Includes resistance simulations
  - Includes voltage and expansion simulations
- Run [figures_1.ipynb](./degradation_model/figures_1.ipynb) to generate figures from the Results section in the paper
- Run [figures_2.ipynb](./degradation_model/figures_2.ipynb) to generate figures from other sections in the paper
