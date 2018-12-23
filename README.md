# leastcostpath - Version 0.1.1

R Implementation of Least Cost Path Analysis Functions

#### current functions
##### <code>leastcostpath</code> - computes Least Cost Paths using multiple cost functions.</b>

###### Anisotropic Cost Functions -  anisotropic cost functions are dependent on the direction of movement, with the cost of travelling from point A and B not being equal to the cost of travelling from B to A.
 * Tobler's Hiking Function (1993)</b><br /> 
<code>6 * exp(-3.5 * abs(slope[adj] + 0.05))</code><br />
 * Marquez-Perez et al. (2017) Modified Hiking function<br />
<code> 4.8 * exp(-5.3 * abs(slope[adj] * 0.7) + 0.03)</code><br />

###### Isotropic Cost Functions - Isotropic cost functions assume that travel across a surface is neither benefitted nor hindered by the directionality of movement.
 * Llobera and Sluckin (2007) Fourth-degree polynomial function<br /> 
<code>1/(1 + abs(slope[adj]/crit_slope)^2)</code><br /><br />

##### <code>validation_buffer</code> - computes the accurracy of the Least Cost Path relative to another SpatialLine* object based on method proposed by Goodchild and Hunter (1997).

#### Future functions
* Incorporate 24 neighbours within LCP calculation. 60% complete.
* Implement validation method based on the distance from the optimal route (ie. straight line) and the LCP. 20% complete
* Incorporation of flow maps as method to visualise Least Cost Path accuracy

# Installation

<code>#install.packages("devtools")</code><br />
<code>library(devtools)</code><br />
<code>install_github("josephlewis/leastcostpath")</code><br />
<code>library(leastcostpath)</code>

# History

<code>Version 0.1.0</code> First Release to Github<br />
<code>Version 0.1.1</code> Implemented choice of directionality
