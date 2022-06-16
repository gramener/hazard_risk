# Production Code
This repository is replicating the usecase from the Sunnylives project. This will help to run the trained model on local system

    
    1 CreateTiles.ipynb
        Notebook for tiles creation

    2 GenerateFootprints.ipynb
        Notebook which uses building segmentation model to generate the footprints for a given region

    3 SimplifyFootprints.ipynb
        Notebook which simplifies the footprints

    4 ClassifyFootprints.ipynb
        Notebook which uses roof type classification model to classify roof types for the generated footprints.

    5 FloodRiskScoring.ipynb
        Note generates the riskscoring intermediate and final outputs.   

## Building Segmentation Model
This model is implementated using UNet with efficientnet encoder. Image size required is 512 * 512. The code implementation is available at nn/unet.py


## RoofType Classification Model
The rooft type is done using inception v3. Image size required is 299 * 299. The code implementation is available at nn/classifier.py


## Steps to Run the pipeline

1) Use the environment.yml file to create the environment.
2) Activate the environment in python 
3) Create folder with region_name/input -- Add landsat files, aoi.geojson files and maxar tiff imagery. (for sample use : https://gramener0-my.sharepoint.com/:f:/g/personal/sumedh_ghatage_gramener_com/EnnADtrO7DhAv9f0cPQ9bLABRwQiK3pOV1d9ALxpj4fOoA?e=TXedck)
4) The the notebooks step wise as mentioned in the above sequence

# License
[MIT LICENSE] (https://opensource.org/licenses/MIT)

