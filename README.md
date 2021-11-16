# JupyterNotebooks-and-Anacoda

A lesson about what Jupyter Notebooks and Anaconda can do!

Written by Katie Cochran, Fall 2021

## Installing Necessary Software

Follow these links to install Anaconda, an environment manager, onto your machine, [Windows](https://docs.anaconda.com/anaconda/install/windows/) or [Mac](https://docs.anaconda.com/anaconda/install/mac-os/)

All prompts you see are fine to click "I Accept" or "Next" for, you should not have to change anything in any of the windows. 
If you are having some issues, here is a [link](https://medium.com/@GalarnykMichael/install-python-anaconda-on-windows-2020-f8e188f9a63d) that goes through all of the steps and what they mean! 

Once Anaconda is installed, you can go to the search bar at the bottom of your screen (or click the windows key) and type "anaconda". You should see something come up called the Anaconda Prompt. This is like Command Prompt (CMD), but it is specifically for Anaconda commands and manipulation of environments in the Anaconda environment manager.

![image](https://user-images.githubusercontent.com/50416928/141778323-dbe2f280-2740-4b4e-bc9a-5097f3b8e982.png)

## Configuring an environment in Anaconda

The first thing we will do is make a new enviornment workspace to code in. We can do this by typing in this command into the Anaconda Prompt:
`conda create --name NAME_HERE`

![image](https://user-images.githubusercontent.com/50416928/141778447-3168e9ec-1ef7-4649-b14b-7912157bb0ad.png)

This will create an environment with the name you choose to put in place of NAME_HERE.

To enter this new enviornment, type: `conda activate NAME_HERE`, subsituting the name of your environment in instead of NAME_HERE.

![image](https://user-images.githubusercontent.com/50416928/141778499-71a4a3e3-1878-4ed6-86c1-2a58d5121dd8.png)

## Installing matplotlib and pandas, or any package or library

To install any package or library you wish to use in your environment, once you have activated your environment, type: `conda install PACKAGE_NAME`. This will install the requested package if it is available. You may have to type 'y' and hit the enter key to confirm you want to install it.

We will talk about these two packages in depth later, but for now install them so we can use them!

To install matplotlib, type: `conda install matplotlib`
![image](https://user-images.githubusercontent.com/50416928/141779281-bc8052af-151f-4702-936e-3ebe5a95e185.png)

To install pandas, type: `conda install pandas`
![image](https://user-images.githubusercontent.com/50416928/141779410-07a1da4d-8454-47d9-a052-3d24c971fb71.png)

If you would like to explore either of these libraries, the documentation for matplotlib can be found [here](https://matplotlib.org/stable/contents.html) and the documentation for pandas can be found [here](https://pandas.pydata.org/docs/).

## Installing Jupyter

Jupyter is a software that allows you to create "Notebooks" that contain code cells and markdown cells. We will go over this in depth later, but it is the main part of what we are learning about in this lesson. Anaconda just allows us to install Jupyter in an environment, so that anything you do in that environment will not affect anything else on your computer. This is super helpful for experimenting with code or if you are worried about changing something permanently.

Once you have activated your enviornment, type: `conda install jupyter` to install Jupyter Notebooks.
![image](https://user-images.githubusercontent.com/50416928/141779480-1c7d161e-1322-4739-a601-0b030d9c944d.png)


## Accessing Jupyter Notebooks and Making a Notebook

To access Jupyter Notebooks inside your environment, type: `jupyter notebook`. This will open a new tab in whatever your default browser is. 
![image](https://user-images.githubusercontent.com/50416928/141779762-0489c661-c0c3-46cc-873c-96d04278f787.png)

This new tab will direct you to Jupyter Notebooks automatically. This is not a server available to anyone else online, it is a mirror of what you have in your C drive on your computer. It's comparable to an online and nicely formatted version of File Explorer on Windows or Finder on Mac.
![image](https://user-images.githubusercontent.com/50416928/141779792-5409d8d8-f1f9-4151-be40-88a574a05e48.png)

To make a new notebook, navigate to a folder you'd like the notebook to be in (I made a new folder for this lesson, you can put it anywhere you'd like) and click the "New" button in the upper right hand corner of the screen, and select the Python 3 (kernel) option.
![image](https://user-images.githubusercontent.com/50416928/141779824-726f054c-1f93-46b4-8a05-2551b2950cd4.png)

This creates a new Jupyter Notebook for you to work in.
![image](https://user-images.githubusercontent.com/50416928/141779975-070f5b7a-b5be-4dbc-83ab-4dc47a95e071.png)

## Functions and Uses of Jupyter Notebooks

This may just look like a silly way to code if you are used to using something like Sublime or VSCode. However, Jupyter Notebooks are used by people in the industry today, to create data reports and make their code more readable for more non-technical people who are trying to understand their findings.

### Markdown Cells vs. Code Cells

There are two types of "cells" in a Notebook. They are denoted by either no text on the left side for a Markdown cell, or a "line number" or Kernel execution number on the left side for a code cell.
Markdown Cell:
![image](https://user-images.githubusercontent.com/50416928/141781398-531fe818-9941-4cdf-b565-76c59aa10e61.png)

Code Cell:
![image](https://user-images.githubusercontent.com/50416928/141781436-5d8c2f78-0b3b-44fa-8e65-ceed1c9dd84d.png)

Markdown cells are used for explanations, and can be formatted using Markdown syntax. Look at this [link](https://medium.com/analytics-vidhya/the-ultimate-markdown-guide-for-jupyter-notebook-d5e5abf728fd) to learn about all of the cool things you can do with Markdown in a Jupyter Notebook.

Code cells are for just that: code. Jupyter Notebooks have their own Python kernel which allows you to run Python code inside the notebook. You can do anything in Python that you would normally do in any other Python environment inside one of these code cells.

### Importing Some Data

For this example, we will import the CSV file in this repository into our Notebook to avoid going into API calls and getting access to API keys. This CSV file contains data from Spotify about the album Little Dark Age by the artist MGMT. If you are interested in how I got this data, please refer to the Notebook in this repository titled spotifyCSVData, or go to this [link](https://nbviewer.org/github/hacksu/JupyterNotebooks-and-Anacoda/blob/main/spotifyCSVData.ipynb) for a more viewer-friendly format.

To import this CSV file into our Notebook, we will have to get the path of the CSV file. You can do this by downloading the CSV file from this repository and adding it to the same folder your notebook is in (through File Explorer or Finder), or getting the path for where it is after you download it. Either works!

Once you have the path of the CSV file, to import it into your Notebook, type into a code cell: 
`import json
import pandas as pd` 

After this, press the ctrl and enter keys at the same time to run the cell.

To add another code cell below the import code cell, you can hit the 'b' key and it will automatically add a cell below the current cell. If it is a Markdown cell and you want a code cell, hit the 'y' key and it will change to a code cell. Likewise, if you want a Markdown cell instead of a code cell, type m and it will change to a Markdown cell. 

Type in the new code cell: 
`data = pd.read_csv('spotifyCSVData.csv')`
    
This will load the CSV file into our notebook, and then make it available as a JSON object in a variable called csvFile. If the CSV file is not in the directory of your notebook, you will have to insert the path into the function as well. For example: 

`data = pd.read_csv(r'C:\Users\kathm\code\spotifyCSVData.csv')` if the CSV file was in a folder called 'code'

### Using pandas to make a Data Frame

If we had gotten the data from an API call, it would come in the form of a JSON object. The pandas library cannot plot a JSON object, so we would have to make the data there into something called a Data Frame. A Data Frame is a nicely formatted table that can be parsed by the matplotlib library to plot information. Because we imported a CSV file, the data is already in a Data Frame and should look something like this:

![image](https://user-images.githubusercontent.com/50416928/142035103-1c52693a-4854-4289-95f3-01145221d035.png)

### Using matplotlib to display Data Frame

There are a lot of different plots we can make with matplotlib. To plot any type of graph, the same code is needed. 

First, type: `from matplotlib import pyplot as plt` and run the cell.

Insert another cell below it and type this code:
  `fig1, ax1 = plt.subplots(1, 1, figsize = (10, 10))`

This line of code defines a figure and an axes for us to plot on. The subplots function takes several parameters. The only required parameters are two numbers, one for number of rows and number of columns. This is because you can have multiple graphs on the same set of axes. Because we specified 1, 1, that means there is only one spot to plot. figsize is an optional parameter, which makes the size of all figures plotted 10 "inches" by 10 "inches". "Inches" is an arbitrary measurement in this case because the plot won't actually be 10 inches by 10 inches on the screen, it is just the label that pyplot gives to measure the graph size.

In this example, we will use the data from the CSV file to compare variables called "dancability" and "energy". These are two variables that Spotify calculates based on an algorithm that we unforunately are not privy to. What we do know is that these two variables are something that every track has, and that they vary based on what the track sounds like and other things that Spotify deems important. We are going to create a scatter plot to show this coorelation, if it exists, and to also show what point belonds to what track. 

Type this into the same cell you typed the `fig1, ax1...` code in in your notebook:
`
ax1.scatter(data['danceability'], data['energy'])
plt.xlabel("Danceability")
plt.ylabel("Energy")
plt.title("How are the danceability and energy ratings for the Little Dark Age album tracks related?")
for i, label in enumerate(data['name']):
    plt.annotate(label, (data['danceability'][i]+.002, data['energy'][i]+.002))
plt.show()
`

This is a lot :) This is all syntax from the matplotlib pyplot library, used for plotting different types of graphs. We are using a scatterplot so that we can see each point and how it relates to other points. 

`ax1.scatter(data['danceability'], data['energy'])` makes the actual scatterplot, using the information from the 'dancability' column in our Data Frame as the x axis, and the information from the 'energy' column as the y axis. 

`plt.xlabel("Danceability")` and `plt.ylabel("Energy")` are simply labeling the axes so that someone who didn't code this knows what they are looking at.

`plt.title("How are the dancability and energy ratings for the Little Dark Age album tracks related?")` is giving the graph a title, something you should always have!

`for i, label in enumerate(data['name']):
    plt.annotate(label, (data['danceability'][i]+.002, data['energy'][i]+.002))`
gives the dots on the graph something called jitter. This is a bit of a hard concept to wrap your head around, but it is something that data anaylsts do so that if two dots end up in the same spot, they can be offset so both can be shown without overlapping each other.

`plt.show()` shows the graph nicely without any extra output. And we're done!!

## NBViewer to share Notebook files

Sometimes you might want to share your findings with others. You could share the raw notebook file, but then whoever you share it would have to have some way to view it. This may involve installing Jupyter Notebooks on their own computer, and for someone who may not be as technically inclined as yourself this might be a lot. Instead, you can upload your Notebook file to Github, and past the link leading to it into another website called NBViewer. This website generates another link that displays the Notebook file in the Github repo nicely, and can be shared and accessed by anyone with an internet browser.

Once you have uploaded the notebook file to Github, paste the link to the file in Github into the form on [this](https://nbviewer.org/) website and click the "Go!" button. The next page is the URL to your Notebook, rendered with NBViewer.

## Closing a Notebook file and stopping environment

Because Jupyter Notebook is running on your local machine, if you simply close out of the browser tab the process will continue to run in the background. To properly close the Notebook file tab, go to the "File" tab at the top of the page and select the option "Close and halt". Then, on the file view tab, hit the "Quit" button at the top right of the screen. This will halt all processes related to Jupyter Notebooks on your computer.

To stop the environment in Anaconda, go to the Anaconda Prompt and type: `conda deactivate`. This will stop the environment processes running on your computer. After this, you can either close the Anaconda prompt by click the 'x' in the upper corner of the window, or by typing `exit` in the window and hitting enter, which will close the window for you.

## Further Learning

I taught this lesson with knowledge from one of the classes I am currently in, called Data in Emerging Media and Technology, through the College of Emerging Media and Technology (EMAT). This class is part of my minor, Web Design and Development, also from the College of EMAT. If you are interested in things like this or data science and analysis, I would highly recommend this class! Please feel free to reach out to me on Discord with any questions you have, and Dr. David Silva has also agreed to answer your questions, he is the professor who taught this course. His email is: dsilva2@kent.edu. There are also links below if you'd like to learn about the programs!

[College of Emerging Media and Technology](https://www.kent.edu/emat)   
[Minor](https://www.kent.edu/emat/minor-web-design-development)     
[Class EMAT 22110](http://catalog.kent.edu/colleges/ci/emat/web-design-and-development-minor/#programrequirementstext)


