# Visualize Data Fast | Watson Studio: [Blog](https://medium.com/@jorge_castanon/visualize-data-fast-watson-studio-ae1ec63e9b8f?source=friends_link&sk=c9fc9c85f364bdc221a93c1ae78c26db)

## Step by step instructions to reproduce the visualizations:

1. Download the 1,000-row sample data set from [here](https://ibm.box.com/s/6fltz5ilap8pbwzu2tt1yxil6ldosc9d). The file's name is `thermostat_rebates_by_zip_1000.csv`.

1. Create an account on Watson Studio [cloud](https://www.ibm.com/cloud/watson-studio) or download the desktop version [here](https://www.ibm.com/products/watson-studio-desktop).

1. Open Watson Studio.

1. Click `New project` on the top right to create a new project on Watson Studio.
<img src="https://github.com/IBMDataScience/visualize-data-fast/blob/master/screenshots/1%20create%20project.png">

1. Name your project and click `Create` on the bottom right.

1. Click the `Assets` tab if you are not already there.

1. Upload the `thermostat_rebates_by_zip_1000.csv`, on the right hand side of the screen drop or browse the file.

1. In your project, under `Data assets`, click the data set to see a preview of the data set.

1. Click the `Refine` blue box in the top right to open the data set with the Data Refinery tool.

1. Once the Data Refinery tool is open, navigate to the `Visualizations` tab 

1. Create the histogram:
    1. Select the `Histogram chart` on the CHART TYPES.
    1. Select the column "value" (thermostat rebates in USD) as the `X-axis`.
    1. Un-select the `Show kde curve` and the `Show distribution curve` and choose `Bin width` to be 4.

1. Create the map:
    1. Select column "lng" as the Longitude field and column "lat" as the Latitude field.
    1. Select column "value" (thermostat rebates in USD) as the Size map field.
    1. Zoom-in to the interesting areas of the map.

1. Create the scatterplot woth correlations: 
    1. Select column "value".
    1. Click `Add another column` and select column "median".
    1. Click `Add another column` and select column "mean".
    1. Click `Add another column` and select column "population".
    1. Only strong correlation is between "median" and "mean" which is not surprising (the mean and median household income are similar statistics).
