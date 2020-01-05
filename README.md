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


## Windows machines

First of all, it is required to have a python v 3.6.8 with 64 bits. It can be obtained from [here](https://www.python.org/downloads/windows/).
Probably another pthon versions would work, but 3.8+ has proven to have an issue with pip and tensorflow.

This version includes pip, so it is not necessary to install it.

### Scripts enabling
By default, Powershell does not enable you to execute scripts. So, It is necessary t enable them. 

This command will do, according to [this thread](https://docs.microsoft.com/es-es/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-6)

```Set-ExecutionPolicy -ExecutionPolicy  	Unrestricted-Scope CurrentUser```

# Environment creation and activation

It is recommended to run everything on an environment

```pip install virtualenv```

#### Create virtualenv

```virtualenv path_to_virtual_envs_location/environment_name```

#### Activate virtualenv
This is why we enabled the script execution for the current user.
If we are using cmd, just run this command

```./path_to_virtual_envs_location/environment_name/Scripts/activate.bat```
If we are using powershell, 

```./path_to_virtual_envs_location/environment_name/Scripts/activate.ps1```

### Install requirements
Now we are sourcing our created environment. Just install the requirements:

```pip install -r requirements_windows.txt```

#### Notebook installation
Although it should be contained on the requirements, it is a complete different requirement than on ubuntu. So, it is needed to run this line:
```pip install notebook```

#### Torch
If you want also to install torch, you need to run this line (only for cpu)

```pip install torch==1.3.1+cpu torchvision==0.4.2+cpu -f https://download.pytorch.org/whl/torch_stable.html```

### Jupyter kernel generation
After having sourced the environment: 

```ipython kernel install --user --name=environment_name```

