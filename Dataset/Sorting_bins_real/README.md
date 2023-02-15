# README

The data described here was used in the use case "Quality control on sorting bins using real data", as described <a href="https://ai4im551107933.wordpress.com/use-case-1b-quality-control-on-sorting-bins-using-real-data/">here</a> and in the extended abstract:

[] S. Michiels, C. De Schryver, L. Houthuys, F. Vogeler, F. Desplentere. "Automated quality control in IM manufacturing". Extended abstract accepted and presented at BNAIC/BeneLearn, Mechelen, Belgium, 2022. (<a href="https://bnaic2022.uantwerpen.be/wp-content/uploads/BNAICBeNeLearn_2022_submission_4207.pdf">link</a>)

More information about the data can be found on the website and in the cited abstract.

## Load data

The data can be loaded through the python code:

<pre><code class="python">import numpy as np

x=np.load("x.npy")
y=np.load("y.npy")</code></pre>


## Data structure

### x

The variable x contains seven time-series, over 181 time steps, describing 438 products.

These series were pre-processed in order to, per product, use the same 181 time steps for each series. 

x is a numpy array, where the third dimension represents the specific time series. These are, in order:
<ol>
  <li>Injection pressure [bar]</li>
  <li>Screwvolume cc</li>
  <li>Cavity pressure [bar]</li>
  <li>Cavity temperature out [°C]</li>
  <li>Cavity temperature in [°C]</li>
  <li>Cavity temperature end flow [°C]</li>
</ol>

### y

The variable y contains two labels for each of the 438 products. These are, in order:
<ol>
  <li>Opening distance</li>
  <li>Valid (boolean)</li>
</ol>
