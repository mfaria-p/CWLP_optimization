<h1 align="center">
  <br>
  Capacitated Warehouse Location Problem  
  <br>
  MIP vs CP Solver Comparison
  <br>
</h1>

<p align="center">
  <a href="#Project-Overview">Project Overview</a> •
  <a href="#Project-Structure">Project Structure</a> •
  <a href="#user-instructions">User Instructions</a> •
</p>

<br>

## Project Overview

In this project, we study and compare **Mixed-Integer Programming (MIP)** and **Constraint Programming (CP)** approaches for solving the **Capacitated Warehouse Location Problem (CWLP)**.
The objective is to evaluate the two paradigms in terms of **runtime performance, robustness, and scalability** as problem size and constraint complexity increase.

The project includes:

* A unified Jupyter notebook implementing both MIP and CP models 
* Benchmark CWLP instances in numeric and letter-based formats
* Experimental results for original and extended scenarios
* Performance evaluations and visualizations
* A written report summarizing methodology and findings

<br>

## Project Structure

```
TPC2/
├── README.md                     # Project documentation
├── assignment_code.ipynb          # Main notebook (data loading, model execution and evaluation)
├── Report.pdf                     # Final project report
├── data_num/                      # Numeric CWLP instances
│   └── <instance files>
├── data_let/                      # Letter-based CWLP instances
│   ├── capa*
│   ├── capb*
│   └── capc*
└── outputs/                       # Generated results and plots
    ├── compare_bestcp_vs_mip_original.csv
    ├── compare_bestcp_vs_mip_extended.csv
    ├── results_original_raw.csv
    ├── results_extended_raw.csv
    ├── fig_runtime_cp_original.png
    ├── fig_runtime_cp_extended.png
    └── fig_runtime_mip_vs_dimension.png
```

<br>


## User Instructions

### Install Libraries

This project requires the installation of the `docplex` library. If not previously installed, please remove the `#` as shown below to execute the installation command:

```python
!pip install docplex
```
<br>

### How to Configure Data Paths

The data folders are defined at the beginning of `assignment_code.ipynb`:

```python
CAP_NUM_FOLDER = "data_num"
CAP_LET_FOLDER = "data_let"
```

Ensure these folders exist in the same directory as the notebook and contain the provided instances.

<br>

### How to Run

#### Execute the code

Run all cells sequentially from top to bottom.
The notebook will:

* Load and validate all CWLP instances
* Build and solve MIP and CP models
* Execute original and extended scenarios
* Save raw and aggregated results to the `outputs` folder
* Generate all runtime comparison plots automatically

<br>

After execution, all numerical results and figures used in the report and presentation will be available in the `outputs` folder.

## Authors

- [Mariana Pereira](https://github.com/mfaria-p)
- [Carolina Dias]()
- [Sofia Fernandes]()
