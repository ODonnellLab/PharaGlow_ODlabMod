# Pharaglow install instructions

## with git, github, anaconda, pip already set up

# open temrinal and navigate to the folder in which you want to install th app. I have a git/apps folder in my root directory

# then run the following command:

```bash
git clone https://github.com/ODonnellLab/PharaGlow_ODlabMod.git pharaglow
```

# this will clone the repository to your local folder. navigate into the folder:

```bash
cd Pharaglow
```

# now create a virtual environment using anaconda. imagecodecs needs python>=3.9

```bash
conda create -y --name pumping python=3.12
```
# this creates a virtual environment where you can install specific versions of python tools:

```bash
conda activate pumping
```
# you'll now see (pumping-new) next to your command prompt, indicating the environment is active. 
# to deactivate, run conda deactivate 

# now you need to install the python packages needed to run Pharaglow via PyPi

```bash
python -m pip install pharaglow
```
# install jupyter requirements separately - seems to be necessary to run notebook files now

```bash
pip install jupyter
```
# Then open jupyter lab 

```bash
jupyter lab
```

# this will open a Jupyter lab browswer window from which you can see the PharaGlowMain-testing.ipynb file, which is interactive
# on the top right you need to select the pumping kernel 

# then you need to input the path of the parameters file, and input and output path (folder containing tiff files)

# you can then execute the code blocks one by one

#### need ipywidgets and ipyfilechooser

