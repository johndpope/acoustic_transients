# acoustic_transients

Detect acoustic transient signals template:

- Given a folder with TOL csv files (processed using PAMGuide MATLAB software), for a certian time period it imports the data. 
- It adds broadband SPL which is used to determine which events are classified as loud. 
- Loud events are compared to background noise over 5 minutes (can be changed) 
- Events that are within 0.5 second interval are classified as transient, and other events classified as not transient. 
- Saves the final dataframe down as csv file, includes all TOL levels for analysis of transient/continuous loud events
