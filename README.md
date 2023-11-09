# App-Scheduler Simulator Project
### ***work-in-progress***

Welcome to the app-scheduler simulator. The project's primary goal is to evaluate 
different schedulers in the presence of in-network computing resources.

Similar to other work 
([Omega](https://www.usenix.org/conference/osdi16/technical-sessions/presentation/gog),
[HIRE](https://github.com/mblo/hire-cluster-simulator)), we included different 
elements of clusters. We implemented resources delivered by various entities: 
+ network devices (switches, network appliances), 
+ smartNICs,
+ operating system components (e.g. Extended Berkeley Packet Filters).

We implemented different scheduling algorithms, such as:
+ HIRE
+ Yarn
+ kuberentes scheduler
+ Firnament
+ Alladin
+ app-sched (**our work**)

In terms of network topology, we add support for the most popular ones:
+ fat-tree level-2
+ fat-tree level-3
+ HyperX
+ DragonFly
+ SlimFly

We adopted traces from the [Alibaba set](https://github.com/alibaba/clusterdata) (cluster 
and GPU) to verify our approach, and we prepared the required wrappers for our simulations.

## Setup
The simulator is implemented in Golang and supports the containerization of workloads. 
Currently runs on Ubuntu 22.04 LTS. 
