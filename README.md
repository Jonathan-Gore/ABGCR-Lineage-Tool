## ABGCR Lineage Tool
A Python-based project for visualizing family and clone relationships within a collection of biological specimens, using data from a CSV file.

## How It's Made:

Tech used: Python, pandas, NetworkX, matplotlib

**Reading Data:**\
The code starts by loading a CSV file into a pandas DataFrame. This file contains data fields such as 'Accession', 'InCollection', 'CloneAccession', and 'ParentAccession' which are crucial for establishing nodes and edges in the graph.\
\
**Graph Initialization:**\
A directed graph is initialized using the NetworkX library, which will hold the relationships between different accessions (specimens).\
\
**Node and Edge Creation:**\
As the DataFrame is iterated through, nodes are created for each accession with attributes based on their collection status (either 'InCollection' or not). Nodes for clones and maternal parents are added similarly, with edges representing these relationships. Clone edges are added with a 'clone' relationship, and parental edges with a 'parent' relationship.\
\
**Graph Layout and Visualization:**\
The NetworkX library's layout options (like spring layout) are used to position the nodes in a visually appealing manner. The graph is then plotted using matplotlib, with nodes colored based on their collection status and sized according to their degree, which signifies the number of connections (relationships) each node has.\
Example Usage and Output:\
\
The graph visualization helps in understanding the connectivity and lineage of specimens based on the provided dataset. This can be especially useful in genetic studies or maintaining breeding records in biological research.

## Optimizations
I adjusted the node sizes based on their degree to enhance the visual hierarchy of the graph. This scaling helps in quickly identifying nodes with higher connectivity, which are potentially more significant in the studied lineage.

## Lessons Learned:
Working with graphical data structures required a solid understanding of both biological relationships and graph theory. I learned to manipulate and visualize complex networks in Python, balancing performance with clarity in graphical representations. Moreover, handling CSV data and integrating it seamlessly into a graph structure was a practical lesson in data transformation and visualization.