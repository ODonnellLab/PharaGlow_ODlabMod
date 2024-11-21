Pharaglow install instructions

with git, github, anaconda, pip already set up

You will need to install juptyerlab which you'll use to run the notebooks, within terminal:

```bash
pip install jupyterlab
```

Now navigate to the folder in which you want to install the app. I have a git/apps folder in my root directory

then run the following command:

```bash
git clone https://github.com/ODonnellLab/PharaGlow_ODlabMod.git pharaglow
```

this will clone the repository to your local folder. navigate into the folder:

```bash
cd pharaglow
```

now create a virtual environment using anaconda. imagecodecs needs python>=3.9

```bash
conda create -y --name pumping python=3.12
```

this creates a virtual environment where you can install specific versions of python tools:

```bash
conda activate pumping
```

you'll now see (pumping-new) next to your command prompt, indicating the environment is active. 
to deactivate (don't do this yet):

```bash
conda deactivate 
```

now you need to install the python packages needed to run Pharaglow via PyPi

```bash
pip install -e .
```
pharaglow should be installed. Make a dedicated kernel so you can run this outside of the conda environment:

```bash
python -m ipykernel install --user --name pumping --display-name "Python (pumping)"
```

Now you can exit the pumping env and run the notebooks from your base environment:

```bash
conda deactivate 
```

To open a notebook:

```bash
jupyter lab
```

this will open a Jupyter lab browswer window from which you can see the PharaGlowMain-testing.ipynb file, which is interactive
on the top right you need to select the pumping kernel 

then you need to input the path of the parameters file, and input and output path (folder containing tiff files)
you can then execute the code blocks one by one

