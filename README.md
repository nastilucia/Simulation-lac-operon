# Simulation-lac-operon
Stochastic simulation of lac operon (Gillespie's algorithm)  

# Prerequisite

- **Python** with a version 2.7 or higher
- **libRoadRunner** with a version 1.5.4 or higher
- **matplotlib** 

# Background
The lac operon is a sequence of six genes in the DNA of E. coli that are responsible for the synthesis of three enzymes involved in the metabolism of lactose. The first three genes of the operon (called \textit{i}, \textit{p}, and \textit{o}) regulate the production of the enzymes, and the last three genes (called \textit{z}, \textit{y}, and \textit{a}, and known as \textit{structural genes}) are transcribed into a single mRNA that is then translated into \textit{beta-galactosidase}, \textit{lactose permease}, the \textit{transacetylase} (the three enzymes). In particular, beta-galactosidase splits lactose into glucose and galactose; lactose permease is a protein that is incorporated in the membrane of the bacterium and actively transports the sugar into the cell; and transacetylase has a marginal role. These three proteins should be synthesized only when lactose is present in the environment.

All the other background information are in the survey: "A survey of gene regulatory networks modelling methods: from differential equations, to Boolean and qualitative bioinspired models" by Roberto Barbuti, Roberta Gori, Paolo Milazzo, and Lucia Nasti. 


# Running the tests

In this simulation, we compare two situations: when lactose is present and when not.
We use the library libroadrunner to study the model. We downloaded it from the Biomodels databse (https://www.ebi.ac.uk/biomodels/BIOMD0000000065)

- `rr` is a reference to libRoadRunner with a file already loaded;
- `rr.model['Lactose']` sets the initial concentration of Lactose in the simulation;
- `rr.simulate()` to simulate the loaded model;
- `rr.setIntegrator('gillespie')` to set the current instance of RoadRunner to use the Gillespie solver.



## Author

* **Lucia Nasti**
