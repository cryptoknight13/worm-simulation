# worm-simulation
Network Infection and Inoculation Simulation Project

To run the program, first, all the functions must be executed then sequentially from top to bottom. Functions used for generating figures for the report are not included in the jupyter notebook.

## Description
This project simulates the spread of a worm through various network topologies and evaluates the effectiveness of different inoculation strategies to mitigate the spread. It leverages Python and the NetworkX library to model the dynamics of infection and inoculation across networks, including Erdös-Rényi, Watts-Strogatz, and Barabási-Albert models.

## Setup and Installation
1. **Python Installation**: Ensure Python 3.6 or newer is installed on your system.
2. **Dependencies**: Install required Python packages using pip:

pip install numpy matplotlib networkx

## Usage
### Running Simulations
-------------------------------------CSV File Generation------------------------------------------------------

Graph Generation
	Function Usage: Utilize the generate_and_save_graph function for creating network graphs.

	Parameters: graph_type, vertices, probability, num_edges, display, filename.
Examples:
	Generate a Barabási graph with 1000 nodes:
	generate_and_save_graph("barabasi", 1000, .3, 2, False, "barabasi_graph_1000.csv")
	Repeat for 5000 and 10000 nodes as needed.
	Program 1: Infection Simulation without Defense
	Load Network: Use load_network_from_csv(csv_file) to load the network from a CSV file.

-------------------------------------------------Program1-----------------------------------------------------

Program 1: Infection Simulation without Defense
	Load Network: Use load_network_from_csv(csv_file) to load the network from a CSV file.

	Simulate Infection: Execute simulate_infection_without_defense(net, patient_zero, infection_probability) to simulate the infection spread without defense.

	Aggregate Results: Call simulation_results_no_cure(csv_file, infection_probabilities, initial_infected_node) for simulations across different probabilities and networks.

	Visualize Results: Use plot_all_infections_by_probability_no_cure(simulation_results_by_probability) to visualize the infection spread under various scenarios.
Steps
	Generate Network Graphs: Create CSV files for networks using generate_and_save_graph.
	Load Networks: Import networks for simulation with load_network_from_csv.
	Run Infection Simulations: Simulate infection spread using simulate_infection_without_defense.
	Aggregate Simulation Results: Gather data across multiple simulations with simulation_results_no_cure.
	Visualize Infection Dynamics: Plot the results with plot_all_infections_by_probability_no_cure.

---------------------------------------------Program2------------------------------------------------------------

Program 2: Simulating Infection with Inoculation
	Function to Simulate: simulate_infection_with_inoculations(net, patient_zero, infection_probability, inoculator, inoculation_probability)
		Simulates infection spread in a network while applying inoculation defenses.
		Parameters: net (network), patient_zero (initial infected node), infection_probability, inoculator (initial inoculation node), inoculation_probability.
	Aggregate Results: simulation_results
		Collects and organizes the outcomes from the simulations for analysis.
	Visualize Outcomes: plot_simulation_results_with_cure(simulation_results)
		Generates visual representations of the simulation data to compare infection dynamics with and without inoculations.
Steps for Execution:
	Prepare Network: Ensure your network data is ready and loaded into the variable net.

	Run Simulation: Execute simulate_infection_with_inoculations with appropriate parameters to model the infection and inoculation process.

	Collect Data: Use the simulation_results to gather and compile data from the simulations.

	Analyze and Visualize: With the collected data, employ plot_simulation_results_with_cure to visualize the effectiveness of inoculation strategies against the spread of infection.


### Plotting Results
Use the plotting functions provided in the scripts to visualize the dynamics of infection and inoculation across rounds. Customize the plotting parameters as needed for detailed analysis.

## Key Components
- **Network Generation**: Scripts for generating networks based on the Erdös-Rényi, Watts-Strogatz, and Barabási-Albert models.
- **Infection Simulation**: A simulation of worm spread through a network without any countermeasures.
- **Inoculation Simulation**: A simulation including a defensive strategy to inoculate nodes and prevent the spread.
- **Adaptive Strategy Simulation**: An advanced simulation that adapts inoculation strategies based on the current network state.
- **Result Analysis and Plotting**: Tools for analyzing and visualizing the results of simulations to compare the effectiveness of different strategies.


## Acknowledgments
- NetworkX for providing the foundational tools for network analysis and simulation.
- Professor and colleagues who have helped improve the project.



