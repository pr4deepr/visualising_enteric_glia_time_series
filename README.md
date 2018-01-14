# Enteric glial activation
I have been interested in visualising time series data from biological experiments in a more interactive manner. 
Plotly has some great tools, so I have used time series data from calcium imaging on gut tissue. 

I used FIJI to pull the numbers out to generate raw traces:

![RAW TRACE](/Raw%20Traces.jpg)

I used IgorPro to analyze the traces. Specifically, I used a script known as [TaroTools](https://sites.google.com/site/tarotoolsregister/) for analysing peaks and defining peak onset times (last timepoint where the slope is negative). 


After calcium imaging, we immunostain the tissue to identify the cells of interest. In this case, the green cells in the graph below. Not all the cells are in focus, so only those with a white overlay are the ones analyzed. The red dots indicate the responsive cells, which appears at the peak onset times extracted using IgorPro.
Purple indicates GFAP immunostaining (expressed by some glial cells) and blue is DAPI (nuclear marker: all cells)

Using plotly, I generated an interactive graph that can be viewed [here](https://plot.ly/~pradeepr/257.embed).

![Interactive Graph](/EGC_interactive.gif)


## Comments

*The reason I used IgorPro is because many of the traces have artefacts that appear as peaks. This is because gut tissue has smooth muscle causing movements during imaging. I have to manually go through the traces and verify the peaks using the image stacks which takes a while :).*

*Will include the code soon*
