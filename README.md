## Developing an Infection Risk ‘Calculator’ to Compare and Analyse the Efficacy of Non-Pharmaceutical Interventions in the Workplace ##

### Aim ###
Respiratory pathogens can cause havoc in a workplace if not managed correctly. 
We aimed to develop a calculator which computes the risk of infection for a given pathogen in a large indoor workplace. 
By implementing different Non-Pharmaceutical Interventions (NPIs), 
we would help to facilitate the devel- opment of new health and safety plans to reduce the risk of infection in a workplace.

### Methods ###
Initial modelling focused on a stochastic and deterministic Susceptible-Infective-Removed (SIR) model, 
which we then adapted by adding extra compartments. We first added an E compartment to account for the latent period, 
and then finally added an A compartment which allows for asymptomatic cases. The final model was a stochastic SEIAR model, 
because even though we are modelling a large indoor workplace, the population size would still not be large enough for a deterministic 
model to be accurate. We also considered the Well’s Riley equation which gives us the probability of infection per time-step for a 
starting number of infectives. Next we considered how different NPIs affected the infection rate, the Well’s Riley equation and 
also the model itself. Finally, we made the calculator using the Gillespie Alogrithm to simulate the stochastic process.

### Results and Conclusions ###
We found that the standard mode of work gave a very high infection probability, 
so implementing inter- ventions was a necessity. For adding singular interventions, 
we found the N95 masks were the best at preventing the virus from spreading, however these masks are often expensive and 
are not widely available to everyone. The next best options were to either wear surgical masks, socially distance or to test every 7 days. 
We found that for the different combinations, ventilation and N95 masks combined were the best at reducing the infection risk. 
However, if ventilation is not a viable option, bubbling and N95 masks would the next best combination.
