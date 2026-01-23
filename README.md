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
  <a href="#authors">Authors</a>
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
* A written report and presentation summarizing methodology and findings

## Project Structure

The directory structure below illustrates the project layout. Note that the `data_` folders must be populated by the user (see [User Instructions](#user-instructions)).

```text
CWLP_optimization/
├── README.md                      # Project documentation
├── assignment_code.ipynb          # Main notebook (data loading, model execution and evaluation)
├── Report.pdf                     # Final project report
├── data_num/                      # Numeric CWLP instances (Sets IV-XIII)
├── data_let/                      # Letter-based CWLP instances (Sets A-C)
└── outputs/                       # Experimental results and generated plots
    ├── compare_bestcp_vs_mip_original.csv
    ├── compare_bestcp_vs_mip_extended.csv
    ├── results_original_raw.csv
    ├── results_extended_raw.csv
    ├── fig_runtime_cp_original.png
    ├── fig_runtime_cp_extended.png
    └── fig_runtime_mip_vs_dimension.png

```

## User Instructions

### 1. Install Libraries

This project requires the `docplex` library. If not previously installed, uncomment and run the installation cell in the notebook:

```python
!pip install docplex

```

### 2. Data Acquisition (Required)

The project uses benchmark instances from the [OR-Library (Capacitated Warehouse Location)](https://people.brunel.ac.uk/~mastjjb/jeb/orlib/capinfo.html). You must download and organize them manually for the code to run.

1. **Create Folders:**
In the same directory as `assignment_code.ipynb`, create two folders:
* `data_num/`
* `data_let/`


2. **Download Files:**
Go to the [OR-Library Files](https://people.brunel.ac.uk/~mastjjb/jeb/orlib/files/) and download the following text files into the corresponding folders:
* **Into `data_num/`** (Standard Numeric Sets IV–XIII):
* Files: `cap41`–`cap44`, `cap51`, `cap61`–`cap64`, `cap71`–`cap74`, `cap81`–`cap84`, `cap91`–`cap94`, `cap101`–`cap104`, `cap111`–`cap114`, `cap121`–`cap124`, `cap131`–`cap134`.


* **Into `data_let/`** (Large Letter Sets A–C):
* Files: `capa`, `capb`, `capc`.
* *Note: The notebook's parser automatically handles the specific format of these files.*

### 3. How to Configure Data Paths

The data folders are defined at the beginning of `assignment_code.ipynb`. If you named your folders differently in the previous step, update these variables in the code:

```python
CAP_NUM_FOLDER = "data_num"
CAP_LET_FOLDER = "data_let"

```

### 4. How to Run

**Execute the code**
Run all cells sequentially from top to bottom. The notebook will:

* Load and validate all CWLP instances.
* Build and solve MIP and CP models.
* Run both original and extended scenarios.
* Generate and save all results (CSVs) and plots (PNGs) directly to the `outputs/` folder.

## Authors

- [Mariana Pereira](https://github.com/mfaria-p)
- [Carolina Dias]()
- [Sofia Fernandes]()
