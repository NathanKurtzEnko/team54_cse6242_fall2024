# Description
This is the main repository for the project of Team 54 for CSE6242 during Fall 2024 semester. In this project we are analyzing motorvehicle collisions in New York City from 2012-2023. Our final deliverable will be a Power BI application/dashboard that geographically visualizes collisions during this time period as well as results explanatory and/or predictive models.

Note that the set up sections below assume that you are using a Windows based machine.

Concerning development, team members can individually create their own branches, or collaborate with other on specific developement branches. We can pull development work into the main branch as needed.

# Data
There are two key data sets that we are using: motorvehicle collisions and weather data. 

For car crashes, we downloaded the "Motor Vehicle Collisions - Crashes" data set provided by the New York Police Department. It is available on [Kaggle](https://www.kaggle.com/datasets/joebeachcapital/car-crashes?select=Motor_Vehicle_Collisions_-_Crashes.csv) and [NYC OpenData Portal](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95/about_data) (where it is regularly updated). 

For weather data, we downloaded a subset of the ERA5 hourly data on single levels. This data set represents a reanalysis resource (a combination of observations from weather stations and climatological models), and is temporally (up to hourly) and spatially (up to 0.25x0.25 degrees). The data is available from the [Copernicus Data Store](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview), but this does require an account and API key. Relevant data has already been downloaded to `./data` directory of this repository.

Additionally, there is one other data source that plays a minor role in cleaning up the collisions and weather sets. This is also accessible via the [NYC OpenData Portal](https://data.cityofnewyork.us/City-Government/Borough-Boundaries/tqmj-j8zm), and can be downloaded in a variety of different formats. For ease of use, it has been downloaded as a `geojson` and stored in the `./data` directory of this repository.

Finally, it might be useful to include linkes to all of the other documents relevant to this project: 

-   [CSE 6242 Project Ideas & Skillsets](https://docs.google.com/spreadsheets/d/1GjJjha1KwdVQAL_elB2NKUw5YVsfgtvG5aHEQeLC62E/edit)

-   [Project Proposal](https://docs.google.com/document/d/1VWa4UL7gkYYmsify6GfOmWTgA2T4GathAvFTH56FLKw/edit)

-   [Proposal Presentation Video](https://www.youtube.com/watch?v=C5zhmqOO_M8)

-   [Proposal Presentation Slides](https://1drv.ms/p/s!Ag6HNmSyUJobhNoHeOv9c_7mx9-XwQ?e=O51beM)

# Setting Up R
If you do not already have R installed and are interested in using it, check out [CRAN](https://cran.r-project.org/) for resources on how to do this.

To help with collaboration, we can use virtual environments. In the case of R, we can use the [`renv`](https://rstudio.github.io/renv/) package. There are a lot of great vignettes about the tools in this package in the package's documentation page. For the sake of brevity, on a few key setup/maintenance functions are listed below. 

You should be able to run all the following commands in your R terminal to set up the virtual environment:

-   Ensure that `renv` is installed in the first place - `install.packages("renv")`

-   Activate the virtual environment - `renv::activate()`

-   Restore the virtual environment - `renv::restore()`

-   Install new packages - `renv::install()`

-   Record newly installed packages - `renv::snapshot()`

Feel free to install other packages that are useful, and record them using `renv` so that others can easily restore that environment. Also, note that a few useful R packages have already been installed for read/handling all types of data as well as model development. Again, feel free to install other things that might be more familiar or useful to you.

# Setting Up Python
If you do not have Python installed and are interested in using it, check out [python.org](https://www.python.org/) or [Anaconda](https://www.anaconda.com/download/). Note that the Python virtual environment was set up using vanilla Python, so for Anaconda folks if this proves problematic, we can figure out how to resolve any issues.

From the terminal, navigate to the main directory of the repository once it has been cloned locally. Then, you should be able to execute the following commands in order to set up/restore the Python virtual environment. 

-   Initialize a virtual environment - `py -m venv <virtual-env-name>`

-   Activate the virtual environment - `./<virtual-env-name>/scripts/activate.bat`

-   Restore environment - `pip install -r requirements.txt`

-   Install new packages - `pip install <package-name>`

-   Record installed packages - `pip freeze > requirements.txt`

Feel free to install other packages that are useful, but note that a few potentially useful ones have already been recorded in the requirements file.

# Quarto
[Quarto](https://quarto.org/) is a language agnostic command-line tool that allows users to write notebook/markdown style documents with a combination of different programming languages. The main file format of Quarto documents is a `.qmd` file. 

Given that some team members are more comfortable using Python, and other moreso with R, this could be a useful tool for collaboration. However, since the scope/duration of the project is relatively small/short, this could be unecessary. Nonetheless, it remains an option, and instructions for downloading/installing/using it can be found in the link above.

# Other Notes
There are a lot of tools that will be used in this project, and not everyone might be incredibly familiar with them. So, linked below are a few resources which might be useful for helping folks understand different things that people are using to do their analysis (please feel free to add to this).

-   Hadley Wickam's (prolific R developer & author) website with info & book recommendations: https://hadley.nz/

-   Tidyverse framework for data science in R: https://www.tidyverse.org/

-   Tidymodels framework for data modeling pipelines in the tidyverse in R (few book recommendations listed here): https://www.tidymodels.org/

-   Spatial data analysis tools & books in R: https://r-spatial.org/

-   A quick overview of Python: https://jakevdp.github.io/WhirlwindTourOfPython/

-   A quick review of data science tools in Python: https://jakevdp.github.io/WhirlwindTourOfPython/

-   Geographic data science with Python: https://geographicdata.science/book/intro.html

-   The GIT reference: https://git-scm.com/docs