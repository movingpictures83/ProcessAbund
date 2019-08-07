# rawAnalysis
A PluMA pipeline designed to process a large-scale CSV file that contains multiple samples,
each belonging to a different class of individual for analysis.

The pipeline begins by taking the original dataset and normalizing the data within each row.
It then thresholds the input data by removing all observables with a frequency lower than 100
across the entire dataset.  Finally, it splits the dataset into four subsets, with specific
values for the Group and the Status (columns 1 and 2).

All of these parameters can be tweaked accordingly, in the input files (*.txt).


To run this pipeline:

1. Clone this repository into the pipelines/ directory of PluMA.
2. Run ./getPlugins.sh to automatically download all relevant PluMA plugins.
3. cd ..
4. scons perl=0 cuda=0
5. ./pluma pipelines/rawAnalysis/config.rawAnalysis.txt

