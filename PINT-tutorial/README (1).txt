This directory contains what you need to run an example three days of observations of the Crab. Most of the setup comes directly from PINT documentation https://nanograv-pint.readthedocs.io/en/latest/timingmodels.html. It's more important to understand the workflow associated with the notebooks. For our purposes, we create windows of observations (we have tried 10 day, 20 day, 40 day and variable day). 

You will need a .par file for the source (generated from Jodrell Bank or ATNF) and a .tim file of TOAs.

1. Create an empty .tim file (ie, window#.tim). 
2. Go into Adding-TOAs.ipynb and add in the first observation .tim file to the empty .tim file.
3. We run the first observation with a .par file directly from Jodrell Bank https://www.jb.man.ac.uk/pulsar/crab.html, fitting for just F0, and the .tim file containing just this day's TOAs. Then save the output.par file.
2. Append the next day's TOAs to the .tim file in Adding-TOAs.ipynb, and use the output.par from Step 1 as the input in PINT. Save the result as output2.par. Watch the rchiq. When it increases above 1, we start fitting for F0 and F1. 
3. Repeat these steps with all remaining data in the observation window. 
4. End goal: Have precise and improved estimates of F0 and F1.


