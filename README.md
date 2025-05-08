# Bias Projection Exercise (FAIRMODE WG5)

This repository includes code for evaluating various techniques to mitigate bias in air quality (AQ) scenarios, with a specific focus on the  FAIRMODE WG5 exercise. Although primarily tailored for this exercise, the methods and tools provided can also be applied more broadly to reduce bias in AQ scenarios beyond the FAIRMODE framework.


Excersise Methodology
----
The aim is to **correct the future scenario (Scenario) based on the BaseCase scenario using the JRC monitoring stations**.

This is achieved through the following steps:

1. **Bias Calculation:**

   * Calculate the bias at the stations as the difference (or ratio) between the observed and modeled values in the BaseCase.

2. **Assigning Bias to Grid Cells:**

   * Assign the bias to the nearest grid cell using Haversine BallTree.

3. **Bias Interpolation over the Grid:**

   * Interpolate the bias from the grid cells to the entire grid using the following methodologies:

     * **Inverse Distance Weighting (IDW) - Additive** 
     * **Inverse Distance Weighting (IDW) - Multiplicative** 
     * **Random Forest Regression with Spatial Features (RFSF)** 

4. **Correction of BaseCase and Scenario:**

   * Apply the interpolated bias to the BaseCase and then to the Scenario to produce the corrected fields.

  
About the FORUM
--
The Forum for Air quality Modeling (FAIRMODE) was launched in 2007 as a joint response initiative of the European Environment Agency (EEA) and the European Commission Joint Research Centre (JRC). The forum is currently chaired by the Joint Research Centre. Its aim is to bring together air quality modelers and users in order to promote and support the harmonized use of models by EU Member States, with emphasis on model application under the European Air Quality Directives.

## UoA Team
- Prof. Bossioli Elissavet 
- Petrides Constantinios

