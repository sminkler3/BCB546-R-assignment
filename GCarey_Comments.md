---
title: "GCarey_Comments"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## Comments

Your script was good overall. I did have to rename some objects (eg. "genotypes" instead of "genotype") to make the script run. However those issues are minor. 
I did notice some issues with your output files. 
Your Chrx_maize_inc files seemed incomplete, with much fewer columns than the teosinte or maize_dec files. I am unsure of the source of this inconsistency. Perhaps there is a small typo somewhere in your script. So far I haven't found it.  
Additionally, none of your files were sorted numerically by position. This was because your Position columns were not numeric. 
You could use a command similar to this to fix that problem: 
```{r}
maize_position$Position = as.numeric(as.character(maize_position$Position))
```
Running the above code will overwrite your current object and make the Position column numeric. After this point you should be able to sort without a problem. 

Apart from these issues, your script is good and seems very smooth and user friendly. Your visualizations are also good. 