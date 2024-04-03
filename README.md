# Inventory routing problem benchmark set

The files in this directory contain all the instances and the solutions obtained by using the algorithms described in  “A Branch-and-Cut Algorithm for a Vendor Managed Inventory Routing Problem” by C. Archetti L. Bertazzi, G. Laporte and M.G. Speranza. There 4 class of instances: 

- Horizon = 3; inventory cost at the supplier equal to 0.03; inventory cost at the retailers: randomly generated in the interval (0.01,0.05) (low cost). 
- Horizon = 3; inventory cost at the supplier equal to 0.3; inventory cost at the retailers: randomly generated in the interval (0.1,0.5) (high cost). 
- Horizon = 6; inventory cost at the supplier equal to 0.03; inventory cost at the retailers: randomly generated in the interval (0.01,0.05) (low cost). 
- Horizon = 6; inventory cost at the supplier equal to 0.3; inventory cost at the retailers: randomly generated in the interval (0.1,0.5) (high cost). 

The format of data files is as follows:

The first line contains the following information: 
n H C np 

where:
- n = number of retailers 
- H = number of discrete time instants of the planning time horizon 
- C = transportation capacity 

The next line contains information concerning the production facility: 
- 1 x_1 y_1 B_1 r_1 h_1

where:
- 1 =  number corresponding to the supplier 
- x_1 = x coordinate of the supplier 
- y_1 = y coordinate of the supplier 
- B_1 = starting level of the inventory at the supplier 
- r_1 = quantity of product made available at supplier at each discrete time instant of the planning time horizon 
- h_1 = unit inventory cost at the supplier 

The next lines contain, for each retailer, the following information: 
- i x_i y_i I_i0 U_i L_i r_i h_i 

where 
- i = retailer number 
- x_i = x coordinate of the retailer i 
- y_i = y coordinate of the retailer i 
- I_i0 = starting level of the inventory at the retailer i 
- U_i = maximum level of the inventory at the retailer I 
- L_i = minimum level of the inventory at the retailer i 
- r_i  = quantity absorbed by the retailer i at each discrete time instant of the planning time horizon 
- h_i = unit inventory cost at the retailer i 

The transportation cost c_{i,j} between the customers i and j is computed as  
- c_{i,j} = INT(euclidean(i,j))

where INT() is a function that rounds its argument to the neareast integer number and euclidean() is a function that computes the euclidean distance between i and j.
