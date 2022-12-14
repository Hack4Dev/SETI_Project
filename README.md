# Search for Extraterrestrial Signals

## Description

The goal of the [Voyager Tutorial](https://github.com/Hack4Dev/SETI_Project/blob/main/VoyagerTutorial.ipynb) is to take you through the "SETI Pipeline", that is the method used by the [Breakthrough Listen](https://seti.berkeley.edu/listen/) team to search for alien techno-signatures! You will take real data gathered by Breakthrough Listen at the [Green Bank Telescope](https://en.wikipedia.org/wiki/Green_Bank_Telescope) in West Virginia, run it through a few algorithms, and see if you can find an alien or two!

Spoiler alert: If you do everything right you WILL find what appears to possibly be an alien! 👽

Second spoiler alert: It's not an alien 😔

But it is the Voyager 1 spacecraft! 🛰️ The farthest human-made object from Earth! Which is still pretty freaking awesome if you ask me!

**The process by which we find Voyager 1 will be nearly identical to the process you will use to search for aliens in other data sets.** So buckle up and listen close: It's time to look for ET!

Click [here](https://www.youtube.com/watch?v=EFxUHoXW1cA) to watch a helpful video about the summer research project that this tutorial is based on.

One of the largest challenges in SETI's search is that human-generated radio frequency interference (RFI) from cell phones, Wi-Fi, radar, etc, is much more abundant and powerful than potential alien-generated signals. Therefore two primary techniques are used to quickly discriminate between human-made RFI and signals from outer space. They're pretty simple, effective, and understanding them is prerequisite for the rest of this tutorial. For a more thorough background discussion, [read through this document](https://github.com/UCBerkeleySETI/breakthrough/tree/master/GBT).

This project does not involve machine learning and therefore can be run locally on your computer.

## Data

For the purpose of simulating what it would be like to find an alien techno-signature, the Breakthrough Listen team used the Green Bank Telescope to observe the signal from the Voyager 1 (launched back in 1977!). We will be working with this data, which was collected by the Greenbank telescope on July 16th, 2020. The data is roughly 300MB and will be downloaded as part of the tutorial.

## Hackathon Task

🛸 Find Your Own Alien!

Congratulations! You've succesfully completed the turboSETI pipeline walkthrough and found an almost-alien! Now that your appetite is whetted, why not search for a real alien?!

Breakthrough Listen has collected huge amounts of data, and we're continually working to refine our processing algorithms, so it's entirely possible there's an alien message that's hiding in the data that's already stored on our servers that's just waiting for you to find it!

That's where you and your spiffy new turboSETI skills come in! Breakthrough Listen is an open-source and open-data project, which means that most of the data it has collected is publicly available! Navigate to http://seti.berkeley.edu/opendata. Then click on "Advanced Search Options" and uncheck all the boxes except for GBT and .hdf5 to make sure that you're getting similar files to the ones we've used in this tutorial. Then pick a dataset--any dataset! Just make sure you pay attention to the file size. You probably don't want to download any Gigabyte-sized files on your own machine...

Now go through the whole turboSETI pipeline: Download an .h5 data file, run turboSETI on it, then run find_event_pipeline on the .dat files from turboSETI and make your plots!

Remember, you can vary the snr and max_drift parameters when running turboSETI to expand/contract your search. You can also vary the find_event_pipeline threshold to include/exclude more RFI. If you find any events at threshold 3, well... maybe let us know ;-) bsrc@berkeley.edu


## Prerequisites

We're going to set up a new "conda environment", which is a collection of python packages that we can import in our code. The environment we create will be called turboSETI, and is described by the file environment.yml (another file in this repository).

## Installation

To create the environment, enter the following in your bash terminal:

### Create the environment from the definition file
conda env create -f environment.yml
### Activate the new environment
conda activate turboSETI
### Create a Jupyter "kernel" for this environment to make it accessible from a notebook
python -m ipykernel install --user --name=turboSETI

Now it's time to move into a Jupyter Notebook! Open this notebook in Jupyter or create a new one to follow along.

You need to select the turboSETI kernel for your notebook by clicking on Kernel > Change Kernel in the top menu of Jupyter.

## Would you like to clone this repository? Feel free!

```bash
> git clone https://github.com/Hack4Dev/SETI_Project.git
```

Then make sure you have the right Python libraries for the tutorials. 


### New to Github?

The easiest way to get all of the lecture and tutorial material is to clone this repository. To do this you need git installed on your laptop. If you're working on Linux you can install git using apt-get (you might need to use sudo):

```
apt install git
```

You can then clone the repository by typing:

```
git clone https://github.com/Hack4Dev/SETI_Project.git
```

To update your clone if changes are made, use:

```
cd SETI_Project/
git pull
```

-----
