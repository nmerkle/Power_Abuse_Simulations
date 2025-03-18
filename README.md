# System dynamics of the abuse of power in science - A mathematical model
                           
How does abuse of power spread in science? What role do whistleblowers, reforms or the silent disappearance of idealistic researchers play? These questions are on the minds of many in science - but what if we could model such dynamics mathematically? Here I present a reaction-diffusion model that describes precisely these processes - based on partial differential equations (PDEs) and simulated with a few lines of code in Python.

The model: Four groups - one dynamic The model distinguishes between four groups of scientists: 
* S(t, u) - Susceptible people who are at risk due to structural or social conditions.
* A(t, u) - People who actively abuse power.
* W(t, u) - Whistleblowers who uncover grievances.
* D(t, u) - People who resign and leave the system. The variables t represent time and u represent spatial dimensions (x, y).

However, other influencing factors or dimensions could also be used and simulated, such as integrity, mental health, career success, narcissism, Machiavellianism or psychopathy of scientists.
The groups shown are linked to each other via reaction and diffusion terms - analogous to models in ecology or epidemiology

# An extract of the central equations

![Formeln](pdes.png)

The terms such as D∇2 stand for spatial diffusion - i.e. the spread of behaviour or influence. Stochastic noise (scandals, random events), e.g. η(t,u) and ξ(t,u), is also part of the model.

# Reforms as a counterforce
A reform term R(D,u) models structural countermeasures - e.g. transparency guidelines, protection systems for whistleblowers or cultural change. From a certain point in time, the pressure for reform sets in and gradually reduces the influence of abusers. This has the effect that reforms slow down the abuse of power, especially when many scientists leave (D) or the system changes. Also the location of a Scientist influences his/her susceptibilty
to whistleblowing or abuse. This can be expressed by the function R(u), where the location on the u = (x, y) axes determine the neighborhood or research environment of the scientist.

# What are the benefits of such a model?
Systemic perspective: We can visualise interactions, e.g. how dropouts and abusers further weaken the system.
Simulate scenarios: What happens without reforms? Or with stronger whistleblower protection?
Stimulate discussion: This model is a tool for reflection - not a dogma, but a way of thinking.

# Code & simulation available
I have implemented the mathematical model as well as the agent-based model in Python. The code is openly accessible and can be extended with further plots:

**[SAWD Simulation Notebook](SAWD_PDEs.ipynb)**
**[Agent_Simulation.ipynb](Agent_Simulation.ipynb)**

# Expansion options 
The simulations can be expanded even further by combining animations with interactive UI elements. This allows parameters to be varied in order to observe how sensitively the system reacts to changes and when stable states are reached. Furthermore, it would be possible to use an agent-based model in conjunction with reinforcement learning to show how agents (also at the micro level) adapt their behaviour through systemic conditions in order to act successfully. While PDEs show systemic trends, an agent-based model could better capture e.g. micro-decisions (and their impacts) of individual agents. A combination would certainly be exciting!


In diesem Zusammenhang habe ich mit der Python-Bibliothek agentpy [0] eine erste Simulation implementiert, die ich im Laufe der Zeit mit Reinforcement Learning-Agenten erweitern möchte.


[0] https://agentpy.readthedocs.io/en/latest/ 
