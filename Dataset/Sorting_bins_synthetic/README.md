# README

The data described here was used in the use case "Quality control on sorting bins using simulated data", as described <a href="https://ai4im551107933.wordpress.com/use-case-1a-quality-control-on-sorting-bins-using-simulated-data/">here</a> and in the paper:

[] S. Michiels, C. De Schryver, L. Houthuys, F. Vogeler, F. Desplentere. "Machine learning for automated quality control in injection moulding manufacturing". In Proceedings of the European Symposium on Artificial Neural Networks (ESANN), Bruges, Belgium, p127-132, 2022. (<a href="https://arxiv.org/abs/2206.15285">link</a> to Arxiv)

More information about the data can be found on the website and in the cited paper.

## Load data

The data can be loaded through the python code:

<pre><code class="python">import numpy as np

x_dict=np.load('x_dict.npy',allow_pickle=True).item()
y_dict=np.load('y_dict.npy',allow_pickle=True).item()</code></pre>

## Data structure

### x_dict

The variable x_dict contains three time-series describing 3147 products, i.e. 'CavityPressure' (pressure in mold sensor over time), 'InjectionPressure' (injection pressure over time) and 'RamPosition' (Ram position over time). 

These series were pre-processed in order to, per product, use the same 200 time steps for each series. 

### y_dict

The variable y_dict contains three labels for each of the 3147 products, i.e. 'opening' (the opening of the “flaps”), 'weight' (the weight of the bin) and 'valid' (whether or not the product is valid).
