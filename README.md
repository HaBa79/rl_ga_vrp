# rl_ga_vrp
We have developed Genetic algorithm with reinforcement learning methods Q-Learning and Deep Q-learning to optimize Vehicle Routing Problem in a better way!
We hope it worked! :)

README MATLAB Implementation of GA-Based and
Reinforcement-Learning-Enhanced Algorithms for the VRP

1.  PROJECT OVERVIEW This directory contains the MATLAB source code and
    input data used to run and evaluate eight algorithms for the Vehicle
    Routing Problem (VRP). The experiments cover three problem sizes:
    small, medium, and large.

The project is organized into: - One Excel workbook in the main (root)
directory, containing the experimental results. - Three subfolders named
“small”, “medium”, and “large”. Each subfolder contains the MATLAB code
and data files for the corresponding problem size.

2.  DIRECTORY STRUCTURE The main directory is organized as follows:

Main/ |– README.txt |– Results.xlsx [Experimental results workbook] |–
small/ | |– MATLAB source files (.m) |
-- MATLAB input data files (.mat) |-- medium/ |   |-- MATLAB source files (.m) |–
MATLAB input data files (.mat)
-- large/     |-- MATLAB source files (.m)– MATLAB input data files
(.mat)

The names of the files inside each size-specific folder follow the same
general organization. The actual input-data filenames may differ
according to the problem instance and its dimensions.

3.  PROBLEM SIZES The experiments are grouped according to the number of
    VRP nodes and vehicles:

-   Small: 10 nodes and 4 vehicles
-   Medium: 50 nodes and 20 vehicles
-   Large: 100 nodes and 40 vehicles

Each of the three folders contains the files associated with its
corresponding problem size.

4.  MATLAB INPUT DATA FILES (.mat) The .mat files contain the input data
    required to execute the algorithms. The screenshot of the
    large-instance folder shows the following example files:

-   Cost_3d_data_100_40.mat
-   D_P_3d_data_100_40.mat
-   V_C_3d_data_100_40.mat
-   V_cost_3d_data_100_40.mat

The suffix “100_40” identifies the large problem instance with 100 nodes
and 40 vehicles. The corresponding data files in the small and medium
folders are associated with their respective problem dimensions.

5.  MATLAB SOURCE FILES (.m) The MATLAB source files are divided into
    two categories.

5.1. Main Algorithm Implementations These files implement the eight
algorithms evaluated in the experiments:

1.  BGA.m — Baseline Genetic Algorithm (Baseline GA)
2.  RAGA.m — Random-Adaptive Genetic Algorithm
3.  QAGA_S.m — Q-learning, Selection-Only
4.  QAGA_R.m — Q-learning, Rate Control
5.  QAGA_F.m — Q-learning, Full Control
6.  QAGA_ES.m — Q-learning, Extended State (256 states)
7.  DQGA_B.m — Deep Q-Network, Discrete State (one-hot, 16 states)
8.  DQGA_C.m — Deep Q-Network, Continuous State (5-dimensional state
    vector)

5.2. Shared Supporting Functions These files provide common operations
and supporting functionality used by the algorithm implementations:

-   Crossover.m — Crossover operation.
-   Mutate.m — Mutation operation.
-   ObjectiveFunction.m — Objective-function evaluation.
-   RankSelection.m — Rank-based selection.
-   RouletteWheelSelection.m — Roulette-wheel selection.
-   TournamentSelection.m — Tournament selection.

These supporting files are not separate optimization algorithms; they
are shared functions called by the main algorithm implementations as
required.

6.  EXPERIMENTAL RESULTS The Excel workbook located in the main
    directory contains the results obtained from 10 independent runs of
    each algorithm for each of the three problem sizes.

The workbook is provided as the consolidated record of the experimental
outcomes. The MATLAB code and input data needed to reproduce the runs
are stored in the corresponding size-specific folders.

7.  HOW TO USE THE FOLDERS To run an experiment:

8.  Open MATLAB.

9.  Set the relevant size-specific folder (small, medium, or large) as
    the working directory, or add that folder to the MATLAB path.

10. Ensure that the required .mat input data files and all relevant .m
    files are available in the MATLAB path.

11. Run the main algorithm file corresponding to the algorithm and
    problem size you want to evaluate.

12. Repeat the procedure for the other algorithms and problem sizes as
    required.

Note: The exact execution settings, input-variable requirements, and
output-saving procedure are defined in the MATLAB source files. Check
the relevant algorithm file before running it.

8.  FILE INVENTORY SUMMARY

-   3 problem-size folders: small, medium, and large.
-   8 main algorithm implementation files (.m) in each size-specific
    folder.
-   6 shared supporting MATLAB function files (.m) in each size-specific
    folder.
-   Input data files (.mat) for the corresponding problem instance in
    each size-specific folder.
-   1 Excel workbook in the main directory containing the results of 10
    runs per algorithm for each problem size.
