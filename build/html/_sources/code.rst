
Code Script
=============

General Description
--------------------

This script aims to compute the aperiodic component from sleep data and explore the findings across different sleep stages. 

Steps:  

1. Load the sleep data and its corresponding hypnogram for all subjects. 

2. Data Cleanup:  

* Epoch the data into 30-second intervals.  

* Extract the hypnogram as a sequence for every 30 seconds to align it with the sleep data.  

3. Power Spectral Density (PSD) Computation: 

* For each channel, compute the Power Spectral Density (PSD) using Welch's method with a median of the 4-second 50% overlap Fast Fourier Transforms (FFTs).  

4. Fit Aperiodic Components:  

* Apply the FOOOF algorithm for each 30-second epoch of the PSD data.  

* Save the results of the FOOOF analysis for the aperiodic and periodic parameters. 

5. Sleep Stage Averaging: 

* Average the aperiodic parameters across N1, N2, N3, and R sleep stages for each channel. 

6. Data Aggregation: 

* Save the averaged aperiodic parameters to a dataframe for further analysis.  

Note:  

* Ensure that the input sleep data and hypnogram files are in the correct format and structure for proper data processing. 

* The script uses FOOOF and PSD to analyze sleep data. Please refer to the respective papers and documentation for more information.  

* Error handling and code comments are included in the script to enhance code clarity and maintainability. 



Code Description
-----------------