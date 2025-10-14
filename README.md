# Overview
Building the C-Dice model discussed in the paper "Climate Clubs: Overcoming Free-riding in International Climate Policy" by William Nordhaus

# Model
n regions attempting to form a stable "Climate Club" coalition. 
Those who join the coalition will raise carbon prices, facing abatement costs
Those who stay out will have tariffs placed on them, based on a trade matrix between the regions
Countries emit CO2 as a costly externality (affecting other nations), and the social cost of carbon is constant at $24/ton


# Algorithm

1) Start with an initial coalition and calculate the net benefits (called the base coalition and base outcomes)
2) Randomly generate a new "Change Coalition" of a set of m regions from the n regions in the model
3) For the regions selected, change their participation status
4) Calculate the net welfare of the change coalition compared to the base coalition for the nations in the change coalition
5) If no nation is worse-off, and at least one country is better-off when making this change, accept the change coalition as the new base coalition
6) Repeat until either the process cycles (a coalition structure repeats) or no other coalition can overturn the base coalition