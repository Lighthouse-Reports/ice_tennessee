# Interior_enforcement
Analysis pipeline for interior enforcement investigation, collaboration between Lighthouse Reports and MoJo

This repo is organized by data source/topic. Topics include things like deportationdata.org datasets, the TN business registry, or the school attendance data.

# Folder structure
Each topic has a separate subfolder in 'data/input', 'data/intermediate', and 'data/results'. Codebooks where data isn't self-explanatory should be included in 'data/input' folders. Similarly each topic should have a separate notebook or script in 'code/preprocessing', 'code/analysis', and 'code/production'. If multiple scripts or notebooks are needed, create a new subfolder with the topic name and put all script pertaining to the topic in that folder.

# Workflow
Pre-processing scripts include scrapers, and data cleaning/wrangling scripts. Cleaning and wrangling scripts should take data stored in a 'data/input' as inputs and store outputs in a 'data/intermediate' folder.

Analysis scripts should take data stored in an intermediate folder (or, if no preprocessing is necessary, in an input folder) and store outputs in a results folder. 

Production scripts, finally, should take results (or other input data) and produce visualizations or tables that can be used for visualizations in published stories (not sure we'll actually need this).

In short, one should only need to download source data into our 'input' folders and then be able to run all scripts iteratively with the outputs produced by the previous script.

# Gitignore
Many input datasets will be too large to store in our repo. I therefore set 'data/input/*' as gitignore. This means it is super important that scripts and notebooks include a link to downloadable source data, which should *always* be on our Google Drive. Then users can simply download the Drive data into an input folder and the entire sequence of scripts should be runnable. We can amend this as needed.

# Pull Requests
Each notebook should be "owned" by one contributor. Changes to notebooks one "owns" can be directly merged to main. If you want to add changes to a notebook owned by somebody else, create a branch and send a pull request to be reviewed by the notebook owner.
