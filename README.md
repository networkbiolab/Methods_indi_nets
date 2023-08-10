# Individualized Coexpression Network Generation

This repository contains scripts for generating individualized coexpression networks based on gene expression data. The coexpression networks are constructed using two different methods: SSN (Specific Sample Network) and CSN (Consensus Coexpression Network).

## Prerequisites

Before using the scripts, ensure that you have the following dependencies installed:

- Python (version 3.6.7)
- numpy (version 1.20.1)
- scipy (version 1.6.2)
- pandas (version 1.2.4)

## Usage

Follow the steps below to generate individualized coexpression networks:

1. Prepare your gene expression data in a matrix format, where rows represent genes and columns represent samples (cells).
   - The data should be a numerical matrix, with headers for the samples (if available).
   - If you have non-numeric headers, ensure that your data includes a separate file with the headers as textdata.

2. Run the script "ssn.py" to generate the Specific Sample Network (SSN).
   - Open a terminal or command prompt and navigate to the directory containing the script.
   - Execute the following command:
     ```
     python ssn.py <input_data_file> <output_file>
     ```
     - Replace `<input_data_file>` with the path to your gene expression data file.
     - Replace `<output_file>` with the desired name for the SSN output file.

3. Run the script "csn.py" to generate the Consensus Specific Network (CSN).
   - Open a terminal or command prompt and navigate to the directory containing the script.
   - Execute the following command:
     ```
     python csn.py <input_data_file> <output_directory>
     ```
     - Replace `<input_data_file>` with the path to your gene expression data file.
     - Replace `<output_directory>` with the desired directory where CSN output files will be saved.

## Input Format

The input gene expression data should be in a matrix format, where each row represents a gene and each column represents a sample (cell). The file should be in a comma-separated values (CSV) format, and the first row should contain headers for the samples (if available).

If your data includes non-numeric headers, please ensure that you provide a separate file named "textdata.txt" that contains the headers in the same order as the columns in the gene expression data file.

## Output Format

The output files generated by the scripts will be in a matrix format, where each row and column represents a gene. The values in the matrix represent the coexpression strengths between genes. The output files can be further analyzed or visualized using various network analysis tools or software.

## Examples

To help you get started, we have included example input files ("example_data.csv" and "example_textdata.txt") and sample commands to run the scripts in the "examples" directory. You can use these as a reference for running the scripts on your own data.

## License

This project is licensed under the [MIT License](LICENSE).
