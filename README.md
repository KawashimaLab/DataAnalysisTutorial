## Data analysis tutorial in Python: KawashimaLab

This is a github repository for data analysis tutorial in Kawashima lab, Weizmann Institute of Science. 

The goal of this class is to learn the basics of data analysis for large-scale calcium imaging experiments. In our experiment, calcium activities of ~100,000 neurons are simuntaneously recorded in the brain of larval zebrafish, which is behaving in a virtual reality environment[ref 1-3]. 

<img src="./pics/maxresdefault.jpg" width="384">


In this class, we use Python as a programming environment. The imaging dataset can be downloaded from thd dropbox (link). 

In this experiment, the fish changes its swim pattern in response to various visual stimuli presented in the environment. We analyze how activities of individual neurons are tuned to different behavioral variables (swim pattern, visual stimuli) and how they are distributed across the brain depending on their tuning.

Below is an except of the demo code. You can find more detailed explanation in the code.

### Data analysis



First, we load the data of behavioral variables, activities of neurons, and positions of neurons.

This data contains data of 6000 neurons which are selected from 100,000 neurons in the original imaging dataset. We use this smaller data for convenience, but if you are interested you can load "" instead to analyze all imaged neurons. 

Then we plot the swim power of fish (Top) and calcium activities of 5 neurons (Bottom) during the experiment.
   
<img src="./pics/swim_power.png" width="960">  
<img src="./pics/neural_response.png" width="960">


We show 3D volume of the imaged brain (Left) or location of selected cells (Right), using projection from the top and the side. Part of the code for these plot is not shown here.
    

| ![imaged_volume](./pics/imaged_volume.png) | ![cell_location](./pics/cell_location.png)  |
|:---:|:---:|

We can also make activity movies of cells to get an intuition.

<img src="./pics/activity_movie_top.gif" width="240">

We calculate correlation coefficients between neural activities and swim patterns and plot them in a whole-brain map. You can see the correlation is different from cell to cell. Some are strongly correlated/anti-correlated to swim pattern, while others are moderately so. 


<img src="./pics/motor_correlation.png" width="480">

We will further practice multivariate regression, dimensionality reduction (PCA, NNMF), clustering (K-means) and other advanced methods for analyzing large-scale neural activity datasets.






### References:

[1] Whole-brain functional imaging at cellular resolution using light-sheet microscopy.
    Ahrens MB, Orger MB, Robson DN, Li JM, Keller PJ; Nature Methods. 
    2013 May;10(5):413-20. doi: 10.1038/nmeth.2434

[2] Mapping brain activity at scale with cluster computing.
    Freeman J, Vladimirov N, Kawashima T, Mu Y, Sofroniew NJ, Bennett DV, Rosen J, Yang C, Looger LL, Ahrens MB
    Nature Methods. 2014 Jul 27;11(9):941-950. doi: 10.1038/nmeth.3041

[3] Light-sheet functional imaging in fictively behaving zebrafish.
    Vladimirov N, Mu Y, Kawashima T, Bennett DV, Yang C, Looger LL, Keller PJ, Freeman J, Ahrens MB
    Nature Methods. 2014 Jul 27;11(9):883-4. doi: 10.1038/nmeth.3040
