# MachineLearningHF

## Prerequisites (fully validated only for MacOs Sierra 10.13.16)

```
sudo apt-get update
sudo apt-get install build-essential
sudo apt-get -y install python3-pip
sudo add-apt-repository ppa:jonathonf/python-3.6
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python3.6
pip3 install jupyter matplotlib numpy pandas scipy scikit-learn
sudo apt-get install git
pip3 install seaborn
sudo apt-get install python3-tk
pip3 install sklearn-evaluation
```

## Prerequisites for Ubuntu (validated for Ubuntu 18.04 at 14/11/18)
### Python 3
This code is based on python3, to install it
```
sudo apt-get update
sudo apt-get install python3.6 python3-tk python3-pip
```
### ROOT with Python 3
It is necessary to build ROOT with python 3.6 while the Ubuntu default is python 2.7, a way to do this using alibuild and update-alternatives is
```
sudo update-alternatives --install /usr/local/bin/python python /usr/bin/python2.7 10
sudo update-alternatives --install /usr/local/bin/python python /usr/bin/python3.6 20
Install alibuild and the python prerequisites of aliBuild with pip3 (instead of pip)
Install the ALICE software normally with aliBuild
```
Then it is possible to switch between python2 and python3 with
```
sudo update-alternatives --config python
```
without affecting ROOT.  
Before running the code the alienv envirovment must be loaded. 

### ML dependencies

```
pip3 install numpy pandas scipy matplotlib seaborn
pip3 install uproot
pip3 install scikit-learn sklearn-evaluation xgboost
pip3 install tensorflow keras
```
To install tensorflow with GPU support please refer to https://www.tensorflow.org/install/gpu

For problems or improvements about Ubuntu prerequisites contact fabio.catalano@cern.ch  

## Produce the ML ntuples and convert it to dataframes

Copy the folder MLDsproductions and put it in your HOME directory. The folder is in the public folder in lxplus below:
```
ginnocen@lxplus.cern.ch:/afs/cern.ch/work/g/ginnocen/public/MLDsproductions
```
Simpy run the following code to perform the ML training creating and convertion:
```
cd ALICEanalysis/buildsample
source buildMLTree.sh
```

## In case of problems:

For problems ginnocen@cern.ch
