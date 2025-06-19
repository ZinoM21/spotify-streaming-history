# Spotify Data Analysis

A Project for SE_25: Data Science @ CODE University of Applied Sciences in Berlin

### Table of contents

- [Description](#description)
- [Tech Stack](#technology-stack)
- [How to Install and Run the application](#how-to-install-and-run-the-application)
- [Credits](#credits)

## Description

In Europe, you have the ability to request your streaming history since the creaion of your Spotify account.

With this project, we exlpored different ways to visualize and get insights of our streaming log, like top listened to tracks or streaming behavior.

We already did this for our own data and our next goal is to build a web app to let other users get the same results with ease.

## Technology Stack

- Language Interpreter / Engine: Python3 & IPython Notebook
- Packages:
  - pandas
  - matplotlib
  - seaborn
  - plotly
  - imageio
  - bar_chart_race

## How to Install and Run the application

### 1. Install python3

You should install a version of python3. On Mac, it should come pre-installed but you should consider updating if you do not have a version of python3 but python2 (check your version by running `python --version` in the command line).

### 2. Create a virtual environment

Because the project will have some required packages like pandas and we do not want to interfere with all the packages on your computer, you have to create a virtual environment. `cd` into the cloned project, then enter `python3 -m venv venv` into the command line.

> Note: It is crucial that you do this step while being in the right directory. This should be a copy of this GitHub repository on your computer.

To activate your virtual environment, type `source venv/bin/activate` on Mac & Linux.

(Be sure deactivate the virtual environment when you want to use the command line like normal again. Run `deactivate` for that. If the comamnd line doesn't show "(venv)" somewhere near the input, it means the environment isn't active.)

### 3. Install all required packages

> Be sure that your virtual environment is activated before this step!

Then run `pip install -r requirements.txt`

This will install all packages that are used in this project automatically. No need to install extra packages.

### 4. Configuration

In `main.py`, set the three constants:

`MODELED_DATA_PATH` => the path to which you want to output your modeled data as parquet file. The default is './out/modeled_data.parquet' and can be left as is.

`EXCLUDE_DEVICES` => if you shared your account with somebody ( xD ), you could exclude their device names here to hide them from your analysis. Leave as None if not applicable.

`AUDIO_FEATURES_PATH` => we support analyzing your streaming history with Spotify's Audio Features API. This path can lead to a file where all audio features off all your songs lie. Note: the API is deprecated, so we dont know how it will work in the future. Therefore this is currently also None and can be left as is.

Also, there are a bunch of lines commented out further down in the main.py file, e.g. with the bar chart races. To minimize load & time consumption, we only have one execution of a bar chart race video in by default. If you want to have more, just uncomment the rows below that you want to have executed, it will just take more time :)

### 5. Run

Run `main.py` to generate plots!

### 6. CLI

Run main.py from terminal like this to use CLI flags: `python3 main.py`

`--skip-import`: like the name says, if you already ran main.py once, your modeled data is stored in the /out folder and can be used again

`--import-only`: if you just want your modeled data, without plots. Your data will be stored in the /out folder.

## Credits

Thanks a lot to [CODE University](https://code.berlin) & our lecturer Kristian!
