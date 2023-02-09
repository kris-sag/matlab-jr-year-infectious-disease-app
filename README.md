# matlab-jr-year-infectious-disease-app
Infectious Disease Outbreak app from Junior Undergraduate Year
- roughly pasted from a companion .pdf file required for original project assignment
# Description
Simple models for the spread of an infectious disease involves three everchanging populations:

I. Susceptible Individuals

II. Diseased Individuals

III. Immune Individuals

These three populations can be modeled with a system of ordinary differential equations (ODE):

```math
 \frac{dS}{dt} = -kSD - \beta S + \rho I\\
 ```
 ```math
 \frac{dD}{dt} = kSD - \frac{1}{\tau}D
 ```
 ```math
 \frac{dI}{dt} = \frac{1}{\tau}D - \beta I - \rho I
 ```
 
where k represents the rate of infection in $\text{days}^{-1}$, $\beta$ represents the natural death rate in $\text{days}^{-1}$, $\tau$ represents the average duration of infection in days, and $\rho$ represents the rate of immunity loss in $\text{days}^{-1}$. Should there be no immunity loss, $\rho$ would simply equal zero.

To make sense of this model, one should notice that the populations increase and decrease in size depending on the sizes of all three populations. This model is quite dynamic and is able to reflect intense changes in the beginning of an outbreak as well as steadier conditions as time passes.


# Methods
The application uses the inputs from the editable fields and uses MATLAB's _ode45_ function to solve the system of differential equations. The resulting matrix is plotted as three lines in a graph.

# Instructions and Interface
## Appearance
![appearance](https://user-images.githubusercontent.com/104951062/217685862-d197fd95-d939-4240-9545-5154b2e281da.png)

## Detailed Instructions
The user must input values for the initial conditions, the time span desired, and coefficients for the ODE. The user then selects the location of the legend, after which the user may press the "Graph!" button and display the results on the axes. Any adjustments will be calculated only after "Graph!" is pressed once again.

The Menu interface is used to read information on the model and the inputs. Additionally, this interface can be used to export the matrix data resulting from the _ode45_ function to an Excel file, but only after a graph has been plotted. It is worth noting that the Menu interface utilizes panels instead of dialog boxes.


# Required Files and Additional Info
- disease clipart.png (4KB), infectiousDiseaseOutbreak.mlapp (72KB), ode_partial.png (15KB)
- Application created using MATLAB version R2020a
