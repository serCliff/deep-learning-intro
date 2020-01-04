# Software instalation and previous steps


## Linux machines (ubuntu)
You need to install pip3 on your system
```sudo apt install python3-pip```
#### Instal virtualenv
```pip3 install virtualenv```
#### Create environment
```virtualenv path_to_virtual_envs_location/environment_name```
##### activate virtuelenv (if needed)
```source path_to_virtual_envs_location/environment_name/bin/activate```
#### install dependences
```pip3 install -r requirements.txt```
In case you have cuda installed and configured, just replace tensorflow package with tensorflow-gpu:
```pip3 install -r requirements_gpu.txt```
#### Jupyter kernel generation
After having sourced the environment:
```ipython kernel install --user --name=environment_name```


