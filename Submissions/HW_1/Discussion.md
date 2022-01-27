# Box Model- Excel Exercise

## Discussion Points
*In addition to The Challenge, start thinking about the following ideas:*
1. What are boundary conditions?  Answer this both conceptually and mathematically.
    In the model the boundary conditions are head = 100 for the top and head = 0 for the bottom. These boundary conditions are useful to know where water is moving in the system. Since water will flow from a high hydraulic head to a low hydraulic head these boundary conditions tell us that water is moving from the top of the system ( high head) to the bottom of the system (low head). Additionally, since we are not changing that top boundary condition, we will consistently have a constant head where the top condition stays the same.


2. What are model parameters?  How do they (and don't they) represent the actual subsurface?
   Model parameters are the other variables that constrain the model dynamics. For our system, we have permeability or hydraulic conductivity. This parameter constrains the movement of water through the system by changing how easy it is to flow. 

3. What are steady state conditions and how can they be identified from the Excel model results?
   
   Steady state conditions mean that water is not moving (or not moving) through the system at a constant rate/flux. For our system, we can tell it is steady state because the flux entering a cell is equal to the flux leaving the cell.

4. Can you imagine how the model inputs could be stored in separate files rather than other spreadsheet cells?  Describe the flow of information from a file that describes the other files that contain model-specific information about the system.
   
   Model parameters could be stored in text files or a raster map. For these inputs to work it would be necessary to either overlay the multiple input files over the grid or have a code that can match grid cells to the different gridded input files.


5. What is an iterative solution?  Can you explain it to a hydrologist who is not a modeler?  Can you describe (or imagine) how Excel finds the solution?
   
   An iterative solution is one that needs the input from the surrounding cells to know the answer to the current cell. In our example, the current cell needs to know the answer from the cell above in order to solve the system. To find the solution, the excel model runs through multiple values until the boundary condition at the bottom is met. 

6. What is a direct solution?  What are its (dis)advantages compared to an iterative (numerical) solution?

A direct solution is one that involves directly calculating the answer using an equation. For our example, we directly calculated the flux across the whole system using the boundary conditions, while each cell iteratively calculated the flux. When just using a direct solution we may miss out on changes that occur within the model or even have slight inaccuracies when using just hte direct model. 
   
