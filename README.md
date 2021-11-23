# acoustic_transients

Detect acoustic transient signals template:

- Given a folder with TOL csv files (processed using PAMGuide MATLAB software), for a certain time period it imports the data into Pandas dataframe. 
- It adds broadband SPL which is used to determine which events are classified as loud. 

Broadband SPL = 10 * log10 ( sum of each TOL level { 10 ** (PSD/10) } )  

- Loud events are compared to background noise over 5 minute interval (adaptable).  
- Events that are within 0.5 second interval are classified as transient, and other events classified as not transient or 'continuous'. 
- Saves the final Pandas dataframe down as csv file, includes all TOL levels for further analysis of transient/continuous loud events
