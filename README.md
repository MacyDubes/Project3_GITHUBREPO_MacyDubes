# Project3_GITHUBREPO_MacyDubes
Project #3: Transportation Data Visualization & Simulation
Client: Federal Highway Administration (FHWA)
Engineer: Macy Dubes
Date: March 31, 2026

Project Summary:
This project focuses on the organization, visualization, and simulation of two transportation datasets:
National Household Travel Survey (NHTS): Used to analyze US transportation usage, household demographics, and vehicle fleet characteristics.
Next Generation Simulation (NGSIM): Used to study high-resolution vehicle trajectories and driving behavior.
The main goal of this project was to move beyond Excel analysis by using Python to automate the visualization of transportation trends and to perform a car-following simulation using the Intelligent Driver Model (IDM).

Repository Contents:
NHTS(in).csv: The source data for household travel characteristics.
NGSIM(in).csv: The source data for vehicle trajectory pairs (Leader vs. Follower).
PythonCodeFinal.ipynb: The main Jupyter Notebook containing all python code for analysis and simulation code.
FinalAnnotatedCodeDocument_Project3_MacyDubes.pdf: A breakdown of the python code and what the code does.
ScopeOfWork.pdf: Project planning documents.
Gantt Chart: Excel sheet to track when tasks will get done. (The original gantt chart I turned in was correct, however the project start changed to update to today but before it was correct. Right now my microsoft account is not working and I am in the process of getting it fixed however when I tried to edit the excel sheet to update it 
my screen slowly started going black and I had to restart. I am not able to edit microsoft excels right now however the original one I turned in had the correct dates
but I cannot access it. I still uploaded one but am not sure how it looks.)
Timesheet: Sheet to track progress and tasks got done and how long it took.

User Guide: Running the Analysis
To replicate this analysis, follow these steps within the Jupyter Notebook environment:

Step 1: Environment Initialization
Ensure you have the required libraries installed (pandas, numpy, matplotlib, and seaborn). 
Run the first cell to import these packages and set the theme.

Step 2: Data Input
The code is designed to look for NHTS(in).csv and NGSIM(in).csv in the same directory as the script.
Prompt: The script will load these automatically. If your filenames differ, update the pd.read_csv strings in the second cell.

Step 3: Statistical Visualizations
Execute the NHTS section to generate the vehicle distribution plots.
Variable Selection: The script currently analyzes vehicle_type, vehicle_age, and fuel_type. You can change these variables if you wish to see different trends

Step 4: Selecting a Trajectory for Simulation
Before running the IDM simulation, you must choose which vehicle pair to analyze.
Locate the trajectory_number variable. Change this integer to use different real-world driving scenarios from the NGSIM data.

Step 5: Executing the IDM Simulation
Run the IDM function cell and the Simulation loop.
Logic: The script will perform a Euler-integration loop, updating the follower's position and speed every 0.1 seconds.
Comparison: The final cell will generate a triple-line plot comparing the Leader, the Actual Follower, and the Simulated (IDM) Follower.
