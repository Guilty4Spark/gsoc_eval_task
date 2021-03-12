# Documentation
The following is a slightly modified summary of the evaluation project I undertook. Note that this README file is a more expansive version of the PPTS
and I have also mentioned a few observation and thoughts I obtained as I went through the task. 

I divided my entire evaluation task into three notebook, two of which I have already described in the PPTS. I'll cover more the same here. 

# Data Processing

The first part of any Machine Learning project is to import, clean and pre-process the data. 

THere's nothing much to discuss when it comes to importing the data, it was more or less elementary. Once, the import was done, the dataset was visualized 
using histograms. We noticed that the E1 and pT1 were skewed whereas the eta1 was almost gaussian shaped. It's hard to describe the exact shape of phi1, but it was 
close to being uniform. I proceeded to standardize it, after which it looked something like this. 


![alt text](https://github.com/VANRao-Stack/gsoc_eval_task/blob/main/GSoC/E1_standard.JPG)


We see that E1 and pT1 is still skewed. Now one thing that was suggested as part of Eric Wulff's thesis was to using logarithmic transform on the two columns to 
normalize them. Performing the suggested transformations and then standardizing results in the following dataset. 


![alt text](https://github.com/VANRao-Stack/gsoc_eval_task/blob/main/GSoC/Wulff.png)


Now, although this does normalize the data, I also tried using the Rank Gauss transformation to normalize the data. The data when normalized and standardized using the rank Gauss method looks something like this. 
