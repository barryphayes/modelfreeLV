Author: Anthony O'Malley
Contact: anthonyomalley999@gmail.com
Supervisor: Dr. Barry P. Hayes
Contact: barry.hayes@ucc.ie
Github: https://github.com/barryphayes/modelfreeLV
Date: 28/April/2024

General Structure:
    Nando LV - OpenDSS files and Load Shapes
    Network Analysis.ipynb - used to plot feeders and find loads furthest from feeder
    UpdateLoadShape.ipynb - updates path in OpenDSS files
    Simulator.ipynb - uses py-dss to calculate voltage profiles
    Simulation Results X - voltage profiles obtained via py-dss
    Single_Network_Model.ipynb - explores one network in detail with different models etc.
    Multi_Network_Models.ipynb - applies modelling pipeline to all feeders
    Models - stored regression results
    Documents - contains PDF and LATEX versions of the conference paper and dissertation
    

All python files are .ipynb files, these can be run using juypter notebook (https://www.anaconda.com/download) or google colab (https://colab.google/) with some minor modifications. 



Folder NandoLV contains the orignal load data in .xlsx files and folders that contain CSV versions that have been transformed from the .xlsx files. Each CSV file is a load profile over 25 hours at 5 min resoloution. The LVNetworkModels contain the feeder files in .xls and opendss compatible .txt files.  
This is the source of the data, it also inculdes py-dss tutorils:
https://sites.google.com/view/luisfochoa/research-tools/opendss-training-material
Dissementaion Document:
https://www.researchgate.net/publication/283569482_Dissemination_Document_Low_Voltage_Networks_Models_and_Low_Carbon_Technology_Profiles


Files NandoLV/LVNetworkModels/Network_X/Feeder_X/LoadShapes.txt need to be updated to inculde the local path, the load shape used is overwritten later,  but is nessecary for OpenDSS to run. To acomplish this run UpdateLoadShape.ipynb and replace variable txt with local path. 


Folder Models/Results contains the results for regression accomplished with linear and neural networks as pickled numpy arrays containing dictionaries or predicted and observed values at various LCT penetration levels.
