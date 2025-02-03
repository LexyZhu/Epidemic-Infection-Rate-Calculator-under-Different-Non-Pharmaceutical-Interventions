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
#### SEIAR Model ####
The transmission graph is shown below and can be expressed using ODEs for deterministic version.
<img width="862" alt="Screenshot 2025-02-03 at 15 45 40" src="https://github.com/user-attachments/assets/593fccb2-4b1b-4f5e-b62c-96e0536a03cc" />
<img width="487" alt="Screenshot 2025-02-03 at 15 45 51" src="https://github.com/user-attachments/assets/d654f259-53ba-42eb-89fa-3e2b2b9ff286" />

For the stochastic version, er remove some of the virus connect to the surrounding environment and then use Gillespie’s Algorithm in modelling process.
<img width="661" alt="Screenshot 2025-02-03 at 15 44 49" src="https://github.com/user-attachments/assets/6cbfb300-146c-4577-9933-56c8f6c62a24" />

#### Wells Riley Equations ####
The Well’s Riley equation is commonly used to find the probability an individual will get infected by considering the transmission of an infectious airborne disease. Since the respiratory pathogens we are looking into spread via aerosols, this equation could give more insight into the risk of infection from a pathogen in a large indoor workplace. The equation is given as:
<img width="265" alt="Screenshot 2025-02-03 at 15 49 59" src="https://github.com/user-attachments/assets/866cf86c-534c-4c50-b9e4-08e03c9b842f" />
where P is the probability of infection, C is the number of cases of infection, S is the total number of susceptible people, I is the number of source infectives, q (quanta/hour) is the quantum generation rate of airborne infection, p (meters3/hour) is the pulmonary ventilation rate of a susceptible person, Q (meters3/hour) is the room ventilation rate with clean air and t (hours) is the exposure time interval. The probability of infection here means how likely an individual is to contract the virus in a day, given the initial number of infectives.


### Results and Conclusions ###
We found that the standard mode of work gave a very high infection probability, 
so implementing inter- ventions was a necessity. For adding singular interventions, 
we found the N95 masks were the best at preventing the virus from spreading, however these masks are often expensive and 
are not widely available to everyone. The next best options were to either wear surgical masks, socially distance or to test every 7 days. 
We found that for the different combinations, ventilation and N95 masks combined were the best at reducing the infection risk. 
However, if ventilation is not a viable option, bubbling and N95 masks would the next best combination.

I attached the simulation results of no interventions, N95 masks applied:

<img width="389" alt="Screenshot 2025-02-03 at 15 52 12" src="https://github.com/user-attachments/assets/4b859ef5-fe6f-49af-9145-f19397bd65f8" />
<img width="390" alt="Screenshot 2025-02-03 at 15 52 22" src="https://github.com/user-attachments/assets/4e44fd27-b072-4307-a494-403aab9317e9" />

Here we found, when ventilation and N95 masks are applied, the probability of getting infection is the lowest:
<img width="638" alt="Screenshot 2025-02-03 at 15 54 51" src="https://github.com/user-attachments/assets/253ae06e-6ff5-467e-9b5c-ccf4c2d68beb" />




