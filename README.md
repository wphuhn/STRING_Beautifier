# STRING Protein Interaction Network Beautification Project #

## Overview ##

This is a simple script to plot a STRING protein interaction network analysis
(available at <http://string-db.org>, last accessed 14 March 2019) in a form
suitable for publication.

Requirements:

- Python (version 3.5.2 tested)
- Jupyter Notebook (version 5.7.0 tested)
- networkx (version 1.11 tested)
- visJS2jupyter (version 0.1.16 tested)

## How to Use ##

Input files are taken from the output of the STRING website:

1) Information about proteins/nodes is read from the
   `string_network_coordinates.txt` file, which may be output by clicking the
   "Exports" button, then selecting the "... as simple tabular text output"
   option.
2) Information about interactions/edges is read from the
   `string_interactions.tsv` file, while may be output by clicking the
   "Exports", then selecting the "... network coordinates" option.
3) (Optional) Information about k-means clusters is read from the
   `string_kmeans_clusters.tsv` file, which may be output by clicking the
   "Clusters" button, then selecting the "download" option.

All these files should be located in the root directory of the script.  Examples
may be found in the `Example_Files\` subdirectory.

4) Start up a Jupyter Notebook instance, then run the `STRING_Beautifier.ipynb`
   script.
5) The resulting network may be found in an HTML file, which will be output in
   the root directory of the script and may be opened in a web browser.

## Notes ##

When using k-means clustering, STRING draws dashed lines between clusters and
solid lines within a cluster.  In this script, we instead draw black lines
for edge with a `combined_score` exceeding a user-defined threshhold value and
light grey lines for interactions below this threshhold, as we believe this is
more reflective of the underlying data set.

## Contact Information ##

If you have any questions, please contact William Huhn at
<https://github.com/wphuhn>.
