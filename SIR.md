#The SIR Model

One simple model used to characterise the way diseases spread is the SIR model. SIR is an acronym for Susceptible, Infected, Recovered. These are incidentally the populations you would track in the model. The variable we are most interested in is the amount of people infected. This variable is influenced by an inflow from the susceptible population, and an outflow into the recovered population. The amount of people who get infected by the disease is equal to the transistion rate $\beta$, times the susceptible population $S$ times the infected population $I$, normalized over the size of the population $N$. $\beta$ is a parameter that models the disease by being the product of the average amount of contacts per person per timestep $n$ and the probability of transmission per contact $p$. The amount of people who recover is determined by the product of $\gamma$ times $I$, with $\gamma$ being the inverse of the time a person is infectious in timesteps, $D$.

The total inflow-outflow equation for $\frac{dI}{dt}$ would be given as:
$$ \frac{dI}{dt} = \frac{\beta I S}{N} - \gamma I$$

The behaviour of this system, assuming tha $I(0) > 0)$, would be that $I$ would increase exponentially over time, until $S$ becomes sufficiently small enough to ensure that $\frac{\beta I S}{N} < \gamma I$, as not enough people can become infected fast enough weigh up against the amount of people who recover from the disease.

An extension of the model could be to model specific factors, such as the amount of contacts $n$. We can imagine that if a serious outbreak would occur, people would decrease their average contacts per person per timestep, the rate at which people would do this itself governed by other parameters.
