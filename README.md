# Project overview
Coding with python3.11, this project implements three different algorithms (MIP, CBD, TS) to solve the SMBSAM-OS-2DP problem.
These algorithms can run independently
# Usage
1. Download the instances file through this link: https://github.com/Shirley-biu/The-Instances-used-in-SMBSAM-OS-2DP-problem
2. Select the example to be calculated and modify the parameter "filename" in the python file.
3. Run algorithm files.
# File description
## MIP_all_instances.py
This file is used to solve the MIP model, which is Model 1 in the paper.
## CBD_nogood.py
This file is used to implement the basic CBD algorithm, which contains only no-good cuts.
## CBD_nogood+sbg.py
This file is used to implement the CBD algorithm with acceleration strategy 1.
## CBD_nogood+batch.py
This file is used to implement the CBD algorithm with acceleration strategy 2.
## CBD_nogood+all.py
This file is used to implement the CBD algorithm with acceleration strategy 1 and acceleration strategy 2.
## CBD_MIS_all-layer.py
This file is used to implement the CBD algorithm that includes both no-good cuts and MIS cuts.
## CBD_MIS_one-layer.py
This file is used to implement the CBD algorithm with the MIS-based one-layer search.
## CBD_MIS_two-layer.py
This file is used to implement the CBD algorithm with the MIS-based two-layer search.
## CBD_MIS_two-layer_adapt.py
This file is used to implement the CBD algorithm with the MIS-based dynamic two-layer search.
## ts_blf.py
This file is used to implement the Tabu Search algorithm, which mainly includes:

Initial solution: The initial solution based on rules.

Tabu list management: Record the recently visited solutions to avoid re-searching them.

Neighborhood search: Search for better solutions within the neighborhood.

diversification perturbation strategy: A random perturbation mechanism is triggered when no improvement is observed over a prolonged period.
# Output
## Output of MIP
optimal objective value: The objective function value corresponding to the optimal solution.

run time: The time taken for the model to run.
### If the optimal solution cannot be obtained within the time limit:
best feasible solution: The objective function value corresponding to the best feasible solution solution.

best bound: The current best bound.

MIP gap: The gap between best feasible solution and best bound.
## Output of CBD algorithm:
obj: The objective function value corresponding to the optimal solution.

MP: The iterations of the mater problem.

SP: The iterations of the slave problem.

run time: The time taken for the algorithm to run.

MP run time：The time taken for the master problem to run.

SP run time：The time taken for the slave problem to run.

cuts: The number of cuts added to the master problem.

obj solution: The optimal scheduling solution.

## Output of Tabu Search algorithm:
obj: The objective function value corresponding to the algorithm.

run time: The time taken for the algorithm to run.

iteration: The iterations of the neighborhood search.
