![FAIRsFAIRLogo_Tw](https://user-images.githubusercontent.com/8457675/155348619-05c89247-057a-4607-9a3e-7e9f548b04b3.png) 
# Guide to the FAIRsFAIR Jupyter Notebooks

FAIRsFAIR “Fostering FAIR Data Practices In Europe” has received funding from the European Union’s Horizon 2020 project call H2020-INFRAEOSC-2018-2020 Grant agreement 831558.

[![DOI](https://zenodo.org/badge/462774022.svg)](https://zenodo.org/badge/latestdoi/462774022)

### Acknowledgements

This work is based on a notebook created as part of the FREYA project:  
Petryszak, R., Fenner, M., Lambert, S., Llinares, M. B., & Madden, F. (2020). FREYA PID Graph - Grant Outputs (1.1.1) [Computer software]. DataCite. https://doi.org/10.14454/QAYM-KT26

The second notebook is re-using a resource created by DataCite to demonstrate the impact of machine-actionble data management plans (DMPs) as part of the FAIR Island project:  
Garza, K. (2020). maDMPs Machine Actionable Data Management Plans (maDMPs) demonstration. (1.0.0) [Computer software]. DataCite. https://doi.org/10.14454/W67K-5373

### How does this relate to FAIRsFAIR work
This work is to support T3.3 of FAIRsFAIR and specifically supports the following themes therein:
* Supporting Data Management Planning
* Defining Data Interoperability Frameworks

## What FAIRsFAIR has done

1. Re-using the notebooks that addressed the use cases we are interested in and validating them.

	* Running the notebook on grant outputs in Binder works fine with a different grant number, however the interactive plot of co-authorship relationships across all outputs cannot be created as the library used is not freely available any longer

2. Building on these notebooks and making the following changes:
	* Restructuring the notebooks to improve their readability
	* Adding data validation so any issues with data result in cleaner error messages
	* Changing the package that creates the co-authorship graph to HoloViews and adjusted the code accordingly to ensure the data is structured in a way that this library can read.

3. Making the resulting notebooks available for others to interact using Binder.


### A note on using notebooks on Binder

The Binder Project is an open community that makes it possible to create sharable, interactive, reproducible environments. It is run by a [federation of teams](https://mybinder.readthedocs.io/en/latest/about/federation.html) that provide it as a free to use service.

Because Binder needs to launch an environment as specified by the person that created the repository, it can take a while to have an interactive notebook ready, so please be patient when trying to work with what's provided.

While you can interact with a binderized notebook and change some data to run the scripts for your own use case, these changes will not be saved unless you create your own notebooks including these changes. If you do interact with a notebook and want to save results, we recommend doing so by saving the resulting plots as images or exporting the notebook as a PDF.


### How to use our provided notebooks
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FAIRsFAIR/dcc/HEAD)

#### Funding grant outputs notebook

##### What does it do?
This notebook uses the DataCite GraphQL API to retrieve all outputs of a grant award from European Union to date.

Goal: By the end of this notebook you should be able to:

* Retrieve all outputs of a grant award from a specific funder;
* Plot number of outputs per year-quarter of the grant award duration;
* Display de-duplicated outputs in tabular format, including the number of their citations, views and downloads;
* Plot a pie chart of the number of outputs per resource type;
* Display an interactive chord plot of co-authorship relationships across all outputs;
* Plot a pie chart of the number of outputs per license type;
* Plot an interactive stacked bar plot showing the proportion of outputs of each type issued under a given license type.

##### How can you re-use it?

1. Launch the binder by clicking on the badge [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FAIRsFAIR/dcc/HEAD)
2. Switch to the "classic" notebook view by changing "lab" at end of the URL to "tree"
3. Click on FAIRsFAIR-funding-grant-outputs.ipynb to launch it
4. Run the notebook

![](https://i.imgur.com/3L3gmnl.png)

5. Once the first cell has been run, you have the option to enter a European Commission grant number of your choice. Add that in the text box offered and run the next cell

![](https://i.imgur.com/5BGthdh.png)

6. Once the second cell gives you the success message
```
OK! - I WAS able to retrieve data for the provided grant number which contains outputs.
OK now to run code cells below to show plots
```
you can run any of the following cells to get the output (plot) for the project you are interested in.



#### Resources connected to a DMP

##### What does it do?
This notebook displays in a human-friendly way all of the connections embedded in a maDMP. By the end of this notebook, you will be able to succinctly display the essential components of the maDMP vision using persistent identifiers (PIDs): Open Researcher and Contributor IDs (ORCIDs), funders IDs, organizations Org IDs, and Dataset IDs (DOIs).

##### How can you re-use it?

1. Launch the binder by clicking on the badge [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FAIRsFAIR/dcc/HEAD)

2. Switch to the "classic" notebook view by changing "lab" at end of the URL to "tree"
3. This notebook uses a library called vega which requires some additonal configuration before it can be ran.
	*  Start a new command line terminal by choosing 'Terminal' in the 'New' menu on the top right
	
	![](https://i.imgur.com/EksdeZw.png)
	* Install the vega library using
	`jupyter nbextension install --sys-prefix --py vega`
	* Check that the library is now enabled by using
	`jupyter nbextension list`
	
	![](https://i.imgur.com/J0jlYpy.png)

	* Finish by typing `exit` and closing the terminal tab

4. Click on FAIRsFAIR-resources-connected-to-DMP.ipynb to launch it
5. Run the notebook
![Launch_DMP_notebook](https://user-images.githubusercontent.com/8457675/155540780-46d84e9a-bbed-48d9-8e0c-060a3470c200.png)

6. Once the first cell has been run successfully, you will have the option to enter the DOI of a DMP of your choice and run the next cell to get a graph of outputs, people, funders etc. connected to it (if available)
![DMP_notebook](https://user-images.githubusercontent.com/8457675/155541393-e973b18d-06d0-4571-a7fc-f8792453dadc.png)


### Disclaimer
We do not have any resource to keep these notebooks running, they are provided as is and might lead to errors when any of the dependencies change.
