The files in this directory contain all the instances and the solutions obtained by using the algorithms described in  “A Branch-and-Cut Algorithm for a Vendor Managed Inventory Routing Problem” by C. Archetti L. Bertazzi, G. Laporte and M.G. Speranza. There 4 class of instances: 

Horizon = 3; inventory cost at the supplier equal to 0.03; inventory cost at the retailers: randomly generated in the interval (0.01,0.05) (low cost). 

Horizon = 3; inventory cost at the supplier equal to 0.3; inventory cost at the retailers: randomly generated in the interval (0.1,0.5) (high cost). 

Horizon = 6; inventory cost at the supplier equal to 0.03; inventory cost at the retailers: randomly generated in the interval (0.01,0.05) (low cost). 

Horizon = 6; inventory cost at the supplier equal to 0.3; inventory cost at the retailers: randomly generated in the interval (0.1,0.5) (high cost). 

 

 

The format of data and solution files is as follows: 

 

A) DATA FILES (*.dat) 

 

The first line contains the following information: 

 

n H C np 

where 

n = number of retailers 

H = number of discrete time instants of the planning time horizon 

C  = transportation capacity 

 

 

The next line contains information concerning the production facility: 

 

1 x1 y1 B1 r1 h1 

 

where 

1 =  number corresponding to the supplier 

x1 = x coordinate of the supplier 

y1 = y coordinate of the supplier 

B1 = starting level of the inventory at the supplier 

r1 = quantity of product made available at supplier at each discrete time instant of the planning time horizon 

h1 = unit inventory cost at the supplier 

 

The next lines contain, for each retailer, the following information: 

 

i xi yi Ii0 Ui Li ri hi 

 

where 

i = retailer number 

xi = x coordinate of the retailer i 

yi = y coordinate of the retailer i 

Ii0 = starting level of the inventory at the retailer i 

Ui = maximum level of the inventory at the retailer I 

Li = minimum level of the inventory at the retailer i 

ri  = quantity absorbed by the retailer i at each discrete time instant of the planning time horizon 

hi = unit inventory cost at the retailer i 

 

The transportation cost ci,j between the customers i and j is computed as  

ci,j =, 

where NINT is a function that rounds its argument to the neareast integer number. 
