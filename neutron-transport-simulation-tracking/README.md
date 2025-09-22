# General information 

This project simulates and investigates neutron transport inside different slabs of material, implemented in the Project_3_11020606.ipynb notebook. The emissions, energy consumption and power of the transmission, reflection and absorbsion rates function (plot_T_A_R_thicknesses) in this notebook has been estimated with CodeCarbon, and the results summarised in Jupyter notebook emission_tracking.ipynb

Raw data collected using CodeCarbon is stored in .csv files with filenames formatted as "XXXXXX_neutron_penetration_emissions_NNNNN.csv", where "XXXXXX" represents the date that the data was collected, and "NNNNN" is the number of neutrons simulated, corresponding to the 2nd argument in the plot_T_A_R_thicknesses() function in Project_3_11020606.ipynb. To create these files, CodeCarbon's EmissionsTracker output_file was manually set to the format outlined above, with the date and number of neutrons specified for that particular run. The cell containing the plot_T_A_R_thicknesses() function was then run multiple (approximately 10) times with the same output_file name. With each run, a new row of data is added to the corresponding XXXXXX_neutron_penetration_emissions_NNNNN.csv file. This process is repeated with different neutron numbers (ensuring the output_file name matches the neutron_number function argument). 

## How to run

This repository has been packaged with [https://github.com/astral-sh/uv](uv). 
To run: 

`uv run --with jupyter jupyter lab`
`

## Packaging info

Instructions followed for packaging with [https://github.com/astral-sh/uv](uv). 

`uv init CodeCarbon-examples-sketch`

`uv add jupyter`

`uv add CodeCarbon`

`uv add numpy`

`uv add matplotlib`

`uv add scipy`

`uv add --dev ipykernel`

`uv run ipython kernel install --user --env VIRTUAL_ENV $(pwd)/.venv --name=CodeCarbon-examples-sketch`
