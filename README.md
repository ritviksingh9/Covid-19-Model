# Covid-19-Model

The data that is being used is from Wikipedia's 2020 Coronavirus data for various countries.  Initially, an SIR (Susceptible, Infected, Removed) model was used.  It was then enhanced by adding an extra variable to take into account people who have been exposed to the virus without knowing.  This is known as the SEIR model.

# SIR Model
The model can be described by the following differential equations:

<img src="https://render.githubusercontent.com/render/math?math=\frac{dS}{dt} = -\frac{\beta SI}{N}">
<img src="https://render.githubusercontent.com/render/math?math=\frac{dE}{dt} = \frac{\beta SI}{N} - \gamma I">
<img src="https://render.githubusercontent.com/render/math?math=\frac{dE}{dt} = \frac{dR}{dt} = \gamma I">

The transmission rate, also known as the basic reproductive rate for the virus is then described as 

<img src="https://render.githubusercontent.com/render/math?math=R_{0} = \frac{\beta}{\gamma}">

# SEIR Model
This model has an additional "Exposed" variable that is taken into account.  For the purposes of this model, it was assumed that the birth rate and death rate amongst the Susceptible population was 0.  With this assumption, the formula for the transmission rate remains the same as the SIR model.  The model can then be similar differential equations as shown below, although there are slight modifications to account for the Exposed population as shown:

<img src="https://render.githubusercontent.com/render/math?math=\frac{dS}{dt} = -\frac{\beta SI}{N}">
<img src="https://render.githubusercontent.com/render/math?math=\frac{dE}{dt} = \frac{\beta SI}{N}-\sigma E">
<img src="https://render.githubusercontent.com/render/math?math=\frac{dI}{dt} = \sigma E - \gamma I">
<img src="https://render.githubusercontent.com/render/math?math=\frac{dR}{dt} = \gamma I">

